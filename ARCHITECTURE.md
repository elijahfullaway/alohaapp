# Aloha: plan hangouts - Architecture (DRAFT)

Status: first draft written from planning notes, before any code. Claude Code should review it, correct it and keep it current, and must ask the founder before changing it.

## Principle
The phone app shows screens. The server holds secrets, rules and scheduled jobs. The app never contains keys, calendar tokens or hold logic.

## Parts
- **Phone app (Expo, TypeScript):** screens, forms, local display. Talks only to Supabase.
- **Supabase:** Postgres database with row-level security, logins (Google, Apple, email), server functions, scheduled jobs.
- **Google Calendar API:** read busy times, write tentative and confirmed events on each user's own calendar. Linked in a separate step after sign-in.
- **Notifications:** push through Expo, email through a sending service.
- **Claude API (stage 2):** called from a server function only, with a spending limit.
- **Sentry:** error reports with no calendar details.

## Draft data model
- profiles: name, optional photo, time zone, age confirmed 18+
- connections: two people, status, created by invite
- invites: link token, one-use, expires after 7 days
- lists and list_members: private, user-named, never visible to members
- windows: owner, time range, lengths, call or in person or either, travel range, activity tag, notice setting
- window_audience: which lists or people can see a window, plus per-person overrides
- requests: window, sender, activity, status (pending, accepted, declined, expired, cancelled), sent_at, expires_at
- calendar_connections: provider, chosen calendars, encrypted tokens (server side only)
- activities: list with categories and in person or remote tags, stored in the database
- user_interests and pair_preferences: used for suggestions (stage 2)
- notification_settings and nudge_events: toggles, day and time, opens, requests sent, mutes

## Request lifecycle
- A request can only be made for a time inside a window shared with the sender, and only if it respects the window's notice setting (12 hours default, 4 same day, 1 last-minute).
- Hold length counts from sent_at and runs continuously: smaller of 24 hours and half the time to start, with a floor of 12 hours (day ahead), 1 hour (same day) or 30 minutes (last-minute), never later than 1 hour before start, and 48 hours if more than 7 days away.
- Pending creates a tentative entry on both calendars. If several requests are pending for one window, the owner sees one entry reading "N requests pending".
- Accept: re-check both calendars for conflicts, then confirm. Decline and expire: clear holds and send a neutral notice. Cancel: either person, clears both calendars.
- Removing or blocking a connection quietly cancels pending requests.
- Calendar entry titles are generic and marked private by default.

## Calendar integration
- Sign-in and calendar access are separate permission steps. Ask for the narrowest Google permission that works.
- During the test the Google project is "In production" while unverified (100-user cap). Verification is needed before going further.
- Calendar is optional: without it, holds exist in the app only.

## Notifications and nudges
- Two weekly nudges (Friday and Sunday, about 12:30 pm local time) from a scheduled job. Skipped when there is nothing useful. Suggestions are never repeated.
- Each nudge can be toggled and its day and time changed. Track opens, requests sent from a nudge and mutes.

## Security rules
- Row-level security on every table, with tests that one user cannot read another's data.
- Secrets in environment variables, never in code, never in chat.
- No calendar details in logs or error reports.
- Separate dev and live Supabase projects once testers join. Database changes are recorded as migration files in git.
- A fresh session reviews security before the first test, and a developer friend reviews before the 25-person test.

## Open questions for Claude Code to raise with the founder
- Which email sending service to use.
- How to store and encrypt Google tokens.
- Exact Google permission to request.
- How invite links carry a person through install and sign-up.
