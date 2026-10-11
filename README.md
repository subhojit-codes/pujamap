# PujaMap — free starter project

## Included
- Responsive traditional red/gold layout for tablets and phones.
- OpenStreetMap with sample markers, search and directions.
- Location access only after the user taps a button and grants browser permission.
- One-time location link with coordinates in the URL.
- Live cross-device sharing is deliberately not enabled until a secure backend is configured.

## Important
- The included pandal markers are illustrative sample locations, NOT verified event listings. Replace them with verified local pandal names and coordinates in `index.html`.
- One-time links reveal coordinates to anyone who has the link. Send privately.
- Geolocation normally requires HTTPS (or localhost).
- If map tiles are blocked in a preview, test the deployed HTTPS site and follow OpenStreetMap's tile usage policy.
- Do not use public/open Firebase database rules.

## Publish for free from a tablet
1. Extract this ZIP using your tablet's Files app.
2. Create a GitHub account/repository and upload `index.html` (GitHub's website may be easier with Chrome's Desktop site option).
3. In repository Settings > Pages, enable publishing from the main branch/root folder.
4. Open the HTTPS Pages URL on your tablet. Grant location only when prompted.

## Add real pandals
Edit the `samples` array in `index.html`. Each object needs a verified name, area, latitude and longitude.

## Live sharing next stage
To support friends on different devices, configure Firebase Realtime Database with expiring unguessable session tokens, strict read/write rules, and a revoke/delete action. Never deploy open database rules or put admin/service-account keys in browser code. Firebase free quotas can change. Test link expiry and revocation on two devices before using it.
