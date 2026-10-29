# Aloha: plan hangouts - Instructions for Claude Code

## Read first, every session
1. PROJECT_SUMMARY.md (status, decisions, next steps)
2. ARCHITECTURE.md (how it fits together and the security rules)
3. The product brief (docs/brief.md once added; the original is the document "Aloha: Product Brief (Version 1)")

Then tell the founder, in a few sentences, where we are and what the next step is.

## About the founder
A beginner with minimal coding experience. Explain what you are doing in plain English, define any jargon, and go in small steps. Ask before making big or irreversible changes.

## Stack
- Phone app: Expo (React Native) with TypeScript in strict mode
- Back end: Supabase (database, logins, server functions, scheduled jobs)
- Google Calendar API (version 1 calendar integration)
- Push notifications through Expo, email through a sending service (to be chosen)
- Claude API for the stage 2 AI features (server-side only)
- Sentry for error reporting before the first test

## How we work
- Plan first. Show the plan and wait for approval before writing code for a slice.
- One thin slice at a time. Finish it end to end, test it, commit it, and only then start the next.
- Write tests as you build, especially for hold timing, expiry, time zones, daylight saving and conflict checks.
- Use strict TypeScript, linting and tests. Run them before every commit.
- Commit every time something works, with a clear message. Use a branch for larger changes.
- Show the founder something that works at the end of each chunk of work.
- Two strikes: if a slice fails twice, revert with git, write a short note about what went wrong in PROJECT_SUMMARY.md, and propose a different approach.
- Keep the project small. Do not add features, services or settings that are not in the brief.
- Remind the founder to clear the session between unrelated tasks.

## Security and privacy rules (not negotiable)
- Never put secrets (keys, passwords, tokens) in code or in chat. Use environment files and make sure they are ignored by git.
- Turn on row-level security for every database table and test that one user cannot read another user's data.
- Calendar tokens, the Claude API key, hold and expiry logic, and notifications live on the server side only. The app contains screens, not secrets.
- Read only what is needed. By default use busy and free times, not event titles or details.
- Never write calendar details to logs or error reports.
- No ad or tracking code near calendar data.
- Do not view real users' calendar data while debugging.

## Ask the founder before
- Adding a new service or library, changing the architecture, requesting new Google permissions, changing the data promise, or spending money.

## Ending a session
When the founder says "wrap up": update PROJECT_SUMMARY.md (what was done, what is next, new decisions, open problems), update ARCHITECTURE.md if anything changed, commit and push, and list what changed.

## Reminders to give the founder at each stage
- Before the first test: security review by a fresh session, row-level security tests, secrets check, separate dev and live databases, Sentry.
- Before the 25-person test: developer-friend review, privacy policy published, Google "In production" status, tester instructions, start Google verification.
- Stage 2: API spending limit and no calendar details in logs.
- Before public launch: professional security review, Google verification, trademark check.
