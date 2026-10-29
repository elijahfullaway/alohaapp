# Aloha: plan hangouts. Product Brief (Version 1)

Drafted October 28, 2026. Reviewed by the founder, with all five assumptions accepted, on October 29, 2026. Working name: Aloha (store title: 'Aloha: plan hangouts'). Written from our planning conversation. Items marked (accepted) were assumptions that the founder has confirmed.

## 1. Vision

A private app where busy friends and family share the times they are free, so 'we should hang out' becomes a confirmed plan in a few taps and lands on both calendars.

## 2. Who it is for

Adults 18+ (core audience 23 to 55) who work full time and whose calendars fill with work, sports, kids and errands. First users are the founder's friends and family: at least 25 people in a private test before anyone shares it more widely.

## 3. The problem

People want to meet but rarely follow through. Finding a time takes effort from both sides, replies arrive hours or days apart, and by then the slot is gone. Group chats make it worse. Without a simple way to start, nothing happens.

## 4. Core loop

1.  Connect a calendar and share a few free windows.

2.  Invite a friend by link. They join and see the windows meant for them.

3.  They pick a window and an activity and send a request.

4.  The time is held as tentative on both calendars.

5.  The other person accepts or declines. Accepting makes it a confirmed event on both calendars.

## 5. Version plan

- **Version 1, stage 1** (build first, test with 3 to 5 people, then the full 25): accounts, invite links, windows with private audience lists, requests, tentative holds, Google Calendar connection, activity list with a custom option.

- **Version 1, stage 2** (added during the 25-person test): interest questions at sign-up, weekly nudges, suggested times with 2 to 3 activity ideas, nudge tracking.

- **Version 2:** counter-proposals, group scheduling, time-pattern learning and recurring hangouts, travel-aware suggestions (opt-in), local events, Outlook and iCloud-only calendars, text messages, video-call links, fuller profiles, accepting a request by web link without an account.

- **Version 3:** in-app chat, social feed, public profiles, ads or sponsored suggestions, gamification.

## 6. Sharing and privacy rules

- A free window contains: date and time range, hangout lengths you are open to, call or in person or either, travel range, an optional activity tag, and a notice setting.

- Audience is set per window using private lists you name yourself (grey suggested names, no built-in 'family' or 'close friends') plus per-person overrides. Lists mix friends and family. A person on two lists sees the windows from both. Nobody can see which lists they are on.

- People can request only times inside windows shared with them.

- Either person can disconnect or block. Removing a connection quietly cancels pending requests and clears holds (accepted).

- Data promise: 'We use your calendar only to show your availability and book hangouts. We never sell it, never use it to target ads, and our team never reads it.' AI processing of free and busy times is disclosed in the privacy policy.

## 7. Requests and holds

Notice setting, chosen by the window owner:

- **Day ahead (default):** request at least 12 hours before start.

- **Same day:** at least 4 hours (accepted).

- **Last-minute okay:** at least 1 hour (accepted).

Hold length is counted from the moment the request is sent and runs continuously, with no overnight pause in version 1:

- Day ahead: the smaller of 24 hours and half the time to start, at least 12 hours but never later than 1 hour before start. If the hangout is more than 7 days away, 48 hours.

- Same day: half the time to start, at least 1 hour.

- Last-minute: half the time to start, at least 30 minutes.

- Day-ahead requests get one reminder halfway through the hold.

Outcomes:

- **Accept:** the hold becomes a confirmed event on both calendars. Both calendars are re-checked for conflicts at this moment.

- **Decline:** the sender gets a kind, neutral notice. It never says the time was booked or that another request was accepted.

- **Expire:** holds are cleared on both calendars and the sender gets a neutral notice and can re-send.

- **Several requests for one window:** the owner sees all of them and accepts one. The others get the same neutral decline. Requesters never see who else asked.

- **Cancel:** either person can cancel before the hangout, which clears both calendars and notifies the other neutrally.

- **Version 1 has no counter-proposals.**

## 8. Calendars

- Sign in with Google, Apple or email. Linking a calendar is a separate step, and only Google Calendar is supported in version 1. The calendar is optional: without one, holds are in-app only and nudges use windows only.

- Users choose which calendars the app checks for conflicts and which calendar receives holds.

- A tentative entry appears on both people's real calendars. When several requests are pending for one window, the owner sees one entry reading 'N requests pending'. Entry titles are generic and marked private by default (accepted).

- A buffer (default 30 minutes, adjustable) is kept around existing events.

- For a call hangout, version 1 only adds the call to the calendar. No video link is created.

## 9. Connecting people

- Invites are a link first, with a code as backup. The link is hard to guess, works once and expires after 7 days (accepted).

- A new person sees what was shared before being asked to sign up.

- Each connection has 2 to 3 optional tap-to-answer questions: activities you do together and how often you want to see this person.

- When two people connect, the app asks if they want to plan a hangout now. If the new person has no windows yet, it proposes times they appear free and lets them tap the ones to share.

- Profile in version 1: name, optional photo, time zone set automatically. Age gate at sign-up: 18+ only.

## 10. Activities

Starting list, grouped by category: watch a movie, meal, cafe, bar or pub, shopping, gym, walk, local event, religious events, board games, video games, call, play a sport, beach, hike, concert, party, camping, plus playdate or family activity, park, cook or host at home, and Other (typed by the user). Categories: food and drinks, events, active and outdoors, home and games, remote, family, other. Each activity is tagged in person, remote or both. About six suggestions are shown at a time, with favorites first. The list lives in the database so it can change without an app update.

## 11. AI in version 1 (stage 2)

- Suggests good times from calendars and windows, with 2 to 3 activity ideas per time. The person chooses the actual activity when sending the request.

- Activities a person did not select as interests are never recommended to them. For a pair, activities both selected come first, then the requester's own interests. The full list stays available when sending a request.

- After a few completed hangouts, ideas also draw on what that pair has done and when. This is simple counting, not complex machine learning, and it is only used for that pair.

- Every suggestion can explain why and can be dismissed.

- Not in version 1: travel-aware times, time-pattern learning, recurring hangouts.

## 12. Notifications

Push plus email in version 1, no texts. Two weekly nudges, Friday and Sunday around 12:30 pm in the person's own time zone. Each can be turned off, and the day and time can be changed. A nudge is skipped when there is nothing useful, and suggestions are never repeated. The app tracks opens, requests sent from a nudge and mutes for each nudge.

## 13. Success measures (25-person test, 4 to 6 weeks)

- At least 20 of 25 finish setup (calendar connected and a window shared).

- Each active person connects with at least 2 friends or family.

- At least 20 confirmed hangouts.

- At least half still active in week 4.

## 14. Constraints

- A few hours a day. First small test in about 2 months, full 25-person test closer to 3, all of version 1 closer to 4.

- Budget about \$20 to \$40 a month plus the \$99 Apple account and a domain.

- Stack: Expo (phone app) and Supabase (database and logins). Secrets, calendar tokens, hold logic and AI calls stay on the server side. Google project set to 'In production' while unverified for the test (100-user cap). Full Google verification before wider launch.

## 15. Design direction

Feel: warm, playful, social, clean. Palette: coral \#FF8C70, sun yellow \#FFD36E, sky blue \#B8DDF0, cream \#FFF8ED, plus dark ink \#2B2B33 for text and deeper coral \#C2492B for buttons with white text. Suggested meanings: yellow for pending, coral for confirmed, blue for remote, always paired with an icon or label. References: Yubo (onboarding and animation, with a calmer grown-up tone), Meetup, Clubhouse, Howbout, Tiimo, Grit, Partiful (link invites, less youthful). More references to be added.

## 16. Assumptions (all accepted October 29, 2026)

- Notice minimums of 4 hours (same day) and 1 hour (last-minute).

- Invite links expire after 7 days and work once.

- Removing a connection cancels pending requests.

- Calendar entry titles are generic and private by default.

- Conflicts are re-checked at accept time rather than watched continuously.

## 17. Known risks

- Wider sharing is capped at 100 users until Google verification is complete, so start verification during the test.

- Overnight expiries may annoy people. Revisit after testing.

- Calendar permissions concern some people. Explain plainly and make disconnecting easy.
