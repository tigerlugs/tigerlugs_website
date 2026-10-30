# tigerlugs.com: public versions

Every version that goes live is tagged `public-YYYY-MM-DD-<name>`. To see
exactly what was public, open
`https://github.com/tigerlugs/tigerlugs_website/tree/<tag>`. To restore one,
check out its files and publish them again.

Homepage source: `tool/website/index.template.html` in the app repo.
Legal pages: built from `docs/legal/` by `tool/build_legal_site.py`.

## public-2026-10-29-account-deletion

- /delete-account: explains deleting from the app (Settings > Delete
  Account) with email as a fallback, and the 30-day window to restore by
  signing back in. Lists the launch-list signup among what's deleted.
- /privacy: the account deletion section and retention now describe the
  30-day restore window. Earlier versions said email only.

## public-2026-10-29-waitlist (launch waitlist redesign)

- New homepage built around a launch waitlist, for sharing from Reddit
  (`tigerlugs.com/?ref=reddit` records where each signup came from).
- Headline: "Wear your watches. We'll keep score." (also the app's Welcome
  screen). Eyebrow: "Coming soon to iPhone & Android". No pricing shown.
- The app's light theme (cream, white cards, gold) and the new tiger cub
  art. The cub logo replaces the old Gemini-generated logo, which is
  deleted. The hero cub waves and blinks like the app's Welcome cub.
- Signup card ("Join the launch list"): email plus an optional iPhone or
  Android choice. Saved to Supabase `launch_waitlist` via
  `join_launch_waitlist` (migration 0007, insert-only, repeats ignored, a
  hidden bot trap). The success state shows a share button.
- "A peek inside": a self-playing slideshow of six real features (one-tap
  wear logging, streaks, cost per wear, the virtual watch box, rotation
  insights, bench tools), with arrows, tap and swipe.
- FAQ: launch timing, what we email, privacy, who makes Tiger Lugs.
- Removed claims about features the app doesn't have (serial records,
  market valuations, pressure-test certificates, strap pairing).
- Footer keeps VinDee LLC (California LLC, Vista, CA), support@tigerlugs.com
  and the copyright line. It adds "Not affiliated with any watch brand" and
  links to Privacy, Terms and Delete Account.
- Link preview image (og-image.png), favicon and home-screen icon.
- Privacy policy updated to cover the launch list. The website uses no
  cookies and no analytics.

## public-2026-10-29-legal

- Added /privacy, /terms and /delete-account (full pages). They replace the
  footer pop-ups, whose September text no longer matched what the app
  collects.

## public-2026-09-28-original

- First site: "Elevate your collection with Tiger Lugs", feature cards, the
  original logo, and the footer pop-ups for privacy and terms.
