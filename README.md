# DUO CHALLENGE V2 — flat GitHub package

## What is included in this build
- Playful & Dynamic responsive interface, in English.
- A central bank of **10,000 question records** in `questions.json`, each with an ID, category, difficulty, four answer options, correct-answer index and explanation.
- Twelve content categories. The bank mixes generated calculation, sequence, reasoning, measurement, science-application and programming exercises with curated factual questions.
- Working local solo modes in the interface: Quick Quiz, Color Clash, Sequence Master, Memory Grid, Closest Wins and Bug Hunter.
- Local XP, levels, activity history and seen-question tracking.
- Firebase initialization using the same Firebase project configuration embedded in the previous DUO CHALLENGE build. Anonymous sign-in and basic live room create/join/leave operations use Realtime Database path `rooms/{code}`.
- PWA manifest, service worker and icons.

## Important limitations — please read
- The 10,000 records are structurally generated and checked for unique IDs, exact-unique question prompts, four distinct choices and valid correct-answer indexes. Many arithmetic and application answers are computed by the generator. The bank has **not** undergone expert human review of every item or a full semantic near-duplicate audit. It is not accurate to describe every record as individually hand-written or independently fact-checked.
- Firebase connection uses the existing project's client configuration and anonymous authentication. Whether room operations succeed depends on the Realtime Database security rules already configured in Firebase. No rules were changed by this package.
- The room lobby is live when Firebase rules allow it. Full synchronized gameplay, server-authoritative scoring/anti-cheat, public matchmaking, friends, chat, voice, spectator mode, tournaments and account/profile synchronization are not complete in this build.
- Local XP/history remains stored in this browser and is not yet synchronized to a player account.
- The existing Firebase project and data are not modified by simply uploading these static files. Back up the current GitHub repository before replacing it.

## Flat file layout
All runtime files are at the project root. There are no `data/` or `icons/` subfolders. The question bank and all icons are referenced from the same directory as `index.html`.

## Deploy to the existing GitHub repository
1. Back up/download the current repository first.
2. Upload the contents of this folder to the repository root (not the ZIP file itself, and not an extra nested folder).
3. Keep `index.html` at the repository root.
4. Preserve the existing GitHub Pages branch/folder setting if it already publishes this repository root.
5. After publishing, open the site over HTTPS. PWA installation and the service worker do not work from a local `file://` URL.

## Validation performed for this package
- `questions.json` parsed successfully.
- 10,000 question records, unique IDs and exact-unique prompts checked.
- Every record has four distinct answer strings and a valid correct-answer index.
- JavaScript syntax checked with Node.
- Manifest JSON parsed and all local file references checked.
- Archive checked to confirm the project files are flat inside one project folder.
- No real-browser, multi-device, Firebase permission or full multiplayer test has been performed.
