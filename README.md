# calcwise-config

Remote config for the Calcwise app. The app downloads these two files and caches them.

## calculators.json
Set a calculator (or a whole section) to `false` to hide it. Anything missing stays visible. Ids come from `CALCULATOR_SECTIONS` in the app's `src/calculators/registry.ts`; unknown ids are ignored.

## rates.json
Default interest rate pre-filled for each government scheme (PPF, EPF, SSY, NSC, Post Office MIS, SCSS). Update after each official announcement and bump `asOf`. Values outside 0–100 are ignored.

## Notes
- Edit on GitHub, commit to `main`. GitHub caches raw files for ~5 minutes.
- The app applies a fresh copy on its **next launch** after downloading it, so the home screen never changes mid-session.
- This can only show/hide existing calculators and change default rates. Adding a calculator needs an app update.
- Keep the repo public and never put secrets here.
