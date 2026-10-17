PE League update notes

Included changes
1. Leaderboard remains competition-aware: League table, UCL group standings / knockout bracket, and FA Cup knockout bracket.
2. Home preview no longer shows a misleading combined league table for UCL or FA Cup; it directs users to the correct Leaderboard view.
3. When editing a knockout score after later rounds have already been generated, the app asks for confirmation and removes later rounds that may now be invalid. Admin can then regenerate the correct next round.
4. When a knockout score changes to a draw, the previous winner is cleared and the user must select the correct winner again.
5. Fixed PWA manifest and service-worker icon paths to match the icon files at the project root; bumped service-worker cache to v23 so the updated app can be installed/refreshed.

Before deploying
- Keep a copy of the currently deployed files.
- Export JSON from Settings before replacing files.
- Upload all files from this ZIP to the same GitHub Pages folder (keep filenames and folder structure).
- Open the site and test a League season, a UCL season, and an FA Cup season.
- Test correcting a knockout score after a later round has been generated; confirm the warning and verify the next round must be created again.
- On mobile, reload the site once after deployment so the service worker can refresh its cache.

Validation performed
- JavaScript syntax check passed for inline scripts.
- Manifest icon paths and service-worker precache paths were checked against files in the package.
- This package has not been browser-tested against the user's live Google Sheets endpoint or real production data. Test with an exported backup / test season before relying on it for live fixtures.
