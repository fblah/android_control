# Installation and updates

No installable release is available yet. These instructions describe the planned experience.

1. Download the signed APK from this repository's Releases page once releases are available.
2. Install it using Android's installer.
3. In your own hub's admin portal, generate a device invitation.
4. Scan the QR in the app, compare the verification code, and approve the pending device in the portal.
5. Approve controllers separately on the phone and grant only the permissions they need.

The app will check for updates, verify signed metadata and the APK, and offer installation. Standard Android installation may require confirmation. No GitHub access token should be entered into or bundled with the app.

Anonymous downloads require this repository to be public. Until then, authenticated manual downloads are for development only.
