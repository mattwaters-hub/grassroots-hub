# Grassroots Hub

Public, mobile-first static prototype for grassroots football. Initial coverage: Mid Herts League, Under 12 Division 6, season 2026/27. Test team: Potters Bar United U12 Lions.

## Publish with GitHub Pages

Repository Settings → Pages → Build and deployment → Deploy from a branch → `main` → `/(root)` → Save.

Expected address after a successful Pages build: https://mattwaters-hub.github.io/grassroots-hub/

No build step, dependencies, API keys or backend. All site files belong in the repository root. `.nojekyll` disables Jekyll processing. Relative asset URLs support the repository subpath.

## Run locally

Serve this directory over HTTP, for example `python -m http.server 4173`. Open http://localhost:4173 in a browser. Opening an HTML attachment inside an iOS file preview may restrict JavaScript; use the hosted website in Safari.

## Data provenance and limits

Team-level facts manually checked in the Mitoo website on **28 October 2026**:

- October results: https://mitoofootball.com/FixtResMonth.cfm?TblName=Matches&DivisionID=616&LeagueCode=MHRML2026&MonthNo=10
- November fixtures: https://mitoofootball.com/FixtResMonth.cfm?TblName=Matches&DivisionID=616&LeagueCode=MHRML2026&MonthNo=11
- Season standings: https://mitoofootball.com/LeagueTab.cfm?TblName=Matches&DivisionID=616&LeagueCode=MHRML2026

`data.js` holds 13 teams, 15 October results, 18 November fixtures and the complete 13-team standings snapshot. The standings include September games; match lists do not. November dates with no listed matches are not populated. No venue is inferred from home-team designation. Conflicting kick-off notes are preserved. No player or referee names are copied. No automatic refresh or live Mitoo integration is implemented. Confirm source licensing/permission and a supported data interface before implementing regular automated ingestion.

Independent prototype, not an official club, league or Mitoo service. Text badges are placeholders, not official crests. Other leagues and age groups are planned; search currently covers only this division.

## Features

- Responsive navigation, filters, search, team favourites and standings.
- Favourites saved locally, with a graceful fallback if browser storage is blocked.
- Accessible modal match details, native sharing or selectable copy fallback.
- One-time .ics reminders with Europe/London daylight-saving rules; unknown times use all-day reminders. Reminders are tentative and do not update automatically.
- Home Screen shortcut support. No offline cache or push notifications.
- No analytics, advertising, accounts or collection of personal data.

## Mobile checks before release

Open in Safari on a physical iPhone. Test navigation, keyboard search, team and month selectors, follow/unfollow across reload, dialog close and Escape where available, share sheet, .ics import, sideways standings scroll, and Home Screen launch. Viewport checks on a desktop browser do not constitute physical iPhone/Safari verification.

## Coach workspace preview

Open `#coaches` from the Coaches navigation item. PBU home kick-off drafts support validation, review and local persistence with blocked-storage fallback. The 8 November Knebworth form link is taken from the supplied Mitoo screenshot (FID 10690, home side). No sign-in, Mitoo write operation, confirmation of submission or public-fixture modification is implemented. Team-sheet star means Man of the Match; team sheets are not implemented yet.
