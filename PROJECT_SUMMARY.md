# Aloha: plan hangouts - Project Summary

Last updated: October 28, 2026

**How to use this file:** It is the handoff between sessions. Any new session (a chat or Claude Code) should read this file first, then the product brief, then say where things stand and what the next step is. At the end of every session, update it.

## What this is
A private mobile app (working name Aloha, store title "Aloha: plan hangouts") where busy friends and family share the times they are free, request hangouts inside those times, and confirm them. A pending request holds the time as tentative on both people's calendars. Built by a founder with minimal coding experience, using Claude Design for screens and Claude Code for the build. Full details are in the document "Aloha: Product Brief (Version 1)".

## Where we are
- Planning is complete: discovery questions, competitor and platform research, a roadmap document, and a product brief (version 1).
- An audit of the brief found seven issues. All seven fixes were accepted.
- The founder is reviewing the brief. The Claude Design prompt is ON HOLD until he says he is ready.
- Accounts and tools (Apple Developer, GitHub, Expo, Supabase, domain, Windows tools): status not yet reported.
- No code has been written.

## Next steps, in order
1. Founder reviews the brief and confirms the five assumptions (brief section 16).
2. Write the Claude Design prompt for the first screens and make the prototype.
3. Finalize CLAUDE.md and ARCHITECTURE.md, create the project folder, connect it to GitHub, first commit.
4. Build in thin slices, finishing each before starting the next: (1) sign-in and app running on the phone; (2) invite link and connecting two accounts; (3) Google Calendar connection, one window, viewing a friend's windows; (4) request, accept, decline, tentative holds on calendars; (5) named lists, audience controls, notice setting; (6) hold timing rules and notifications.
5. Small first test (3 to 5 people), then the 25-person test on stage 1, then stage 2 added (interests, nudges, suggestions).

## Key decisions
**Product**
- Audience 18+ (core 23 to 55). First users are friends and family, at least 25 people before wider sharing.
- Version 1 is built in two stages inside the test. Version 2 and 3 features are listed in the brief.
- No counter-proposals and no auto video links in version 1.

**Sharing**
- Free windows contain date and time range, lengths, call or in person or either, travel range, optional activity tag, and a notice setting.
- Audience is set per window using private, user-named lists plus per-person overrides. Lists are never visible to the people in them.
- Invites are a link first, code as backup, one-use, 7-day expiry (assumption).

**Requests and holds**
- Notice setting per window: day ahead (default, 12 hours), same day (4 hours, assumption), last-minute (1 hour, assumption).
- Hold counted from the time the request is sent, running continuously, no overnight pause. Exact rules are in brief section 7.
- Declines and expiries use kind, neutral messages that never mention another request. Requesters never see who else asked.
- Tentative entry on both real calendars, generic private titles (assumption). Conflicts re-checked at accept time.

**Calendars and accounts**
- Sign-in with Google, Apple or email. Only Google Calendar for version 1, and the calendar is optional.
- Google project set to "In production" while unverified for the test (100-user cap). Full verification before wider launch.

**AI and notifications**
- Stage 2: weekly suggestions of times with 2 to 3 activity ideas. Unselected interests are never recommended. History-based ideas use simple counting per pair.
- Nudges Friday and Sunday about 12:30 pm local, adjustable and toggleable, skipped when empty, tracked for opens, requests and mutes.
- Push plus email, no texts in version 1.

**Business and data**
- Free at first, then a paid tier and/or sponsored suggestions (version 3). No ads in versions 1 and 2.
- Calendar data is never sold or used for ads, and no human reads it. AI processing is disclosed.

**Design**
- Warm, playful, social, clean. Palette: #FF8C70, #FFD36E, #B8DDF0, #FFF8ED, plus ink #2B2B33 and deeper coral #C2492B. References: Yubo (calmer tone), Meetup, Clubhouse, Howbout, Tiimo, Grit, Partiful.

**Tech and budget**
- Expo (TypeScript) and Supabase. Secrets, calendar tokens, hold logic and AI calls stay server-side.
- Claude Pro for design and code. Budget about $20 to $40 a month plus $99 Apple account and a domain.
- Timeline: first small test in about 2 months, 25-person test about 3, all of version 1 about 4.

## Assumptions awaiting confirmation
- Same-day notice 4 hours, last-minute notice 1 hour.
- Invite links expire after 7 days and work once.
- Removing a connection cancels pending requests.
- Calendar entry titles are generic and private by default.
- Conflicts are re-checked at accept time.

## Open risks
- Wider sharing is capped at 100 users until Google verification is complete. Start verification during the test.
- Overnight expiries may annoy people. Revisit after testing.
- Calendar permissions concern some people. Explain plainly and make disconnecting easy.

## Reminders by stage
- **Before code:** brief reviewed (in progress), ARCHITECTURE.md approved, repo, CLAUDE.md, this file, quality checks from the first commit.
- **Every session:** read this file, plan first, one small slice, test, commit, update this file, clear.
- **Before the first test:** security pass by a fresh session, row-level security tests, secrets check, separate dev and live databases, Sentry.
- **Before the 25-person test:** developer-friend review, privacy policy published, Google "In production," tester instructions, start Google verification.
- **Stage 2:** API spending limit, no calendar details in logs.
- **Before public launch:** professional security review, Google verification, trademark check, Apple and Google store requirements.

## Session log
- Oct 28, 2026: Planning completed, brief drafted and audited, project files drafted. Next: founder reviews the brief.
