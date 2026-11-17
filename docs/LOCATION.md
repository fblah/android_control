# Location and movement history

This feature requires a hub and Android app release that both support location (hub 0.5.0-dev or newer).

## Enable on your phone

1. Open Android Control and choose **Enable location access**.
2. Grant location permission, then choose **Allow all the time** in Android’s app location permissions. Approximate location works; precise location gives better accuracy.
3. Keep the paired link running. For periodic tracking, separately enable **Record location in the background**.

Location is off by default. Background tracking aims for a fix about every 15 minutes; Android battery restrictions, force-stop, missing GPS/network signal or loss of internet can delay or prevent updates. Use **Disable location access** to stop location sharing, or **STOP ALL PAIRED ACCESS** to pause all remote access. Saved history remains on the hub until cleared.

Your phone’s account and hub administrators can access permitted location information. Other family members cannot. Legacy QR controllers also need their local location permission checkbox enabled on the phone.

## Use the desktop

Open **Location & history** in the browser sidebar.

- **Locate phone** requests a location fix. Allow up to 40 seconds. The phone may fall back to a recent cached Android fix when GPS is unavailable; always check the timestamp and accuracy.
- **Refresh history** reads saved locations, even while the phone is offline. The timeline and zoom controls let you inspect its movement route.
- On hub **0.6.1-dev or newer**, **Open latest in Google Maps** opens the newest available fix. **Copy coordinates** copies its latitude/longitude. The timeline also has **Open selected point in Google Maps** for an older fix. Google receives coordinates when you open the link; the pin is a snapshot, not continuous tracking. Use Locate phone again for an updated fix. No new phone APK is needed for these buttons.
- **Load map tiles** asks before contacting OpenStreetMap for roads and place names. The map provider can infer the geographic area you view. The route works without external tiles.
- Administrators can **Clear older history**, keeping the last day, week, 30-day month or year, or deleting all history. Active tracking can add new points afterward.

History is limited to one year and 40,000 fixes per phone; long routes are sampled to 2,000 displayed points. Cleanup applies to the selected hub. Independently enrolled hubs and backup copies require separate cleanup. Expired points are removed when history is next accessed or updated; there is no separate disk-expiry timer.

## Where location is stored

Live requests and responses use the encrypted device relay. Saved history is deliberately readable by your own hub so a fresh browser login can retrieve it while the phone is offline. The hub encrypts history on disk with a private storage key. A hub administrator or someone with the complete server volume/key can decrypt it. Keep that volume and its backups private.

Do not submit real coordinates, screenshots showing private movement history, hub credentials or QR invitations in public issues.
