# Installation and updates

1. Download `android-control.apk` from the latest [release](https://github.com/fblah/android_control/releases/latest). GitHub sign-in is not required.
2. Open the APK and follow Android’s installation prompts. Allow installation from your browser or file manager if Android asks.
3. In your hub’s private admin portal, select the correct family account and generate a device invitation.
4. Select **Scan hub QR** in the app, review the hub identity and verification code, and approve the pending phone in the admin portal.
5. Once trusted, the phone connects automatically. Browser users sign in with a passkey for their account. The phone trusts that account’s browser sessions and hub administrators for supported features. Grant Android notification access separately if you want notifications. Screen capture and other Android permissions cannot be silently granted.

Accounts are private from other family members. Hub administrators have master access to supported live device features. Use **STOP ALL PAIRED ACCESS** on the phone to pause remote access; **Resume connection** enables it again.

## Updates

Select **Check for app updates** to check manually. Enable **Check GitHub updates when opening the app** for automatic checks. The app verifies signed metadata, download integrity and APK signing identity before offering installation. Android still requires installation approval; updates are not silently installed. Update checks contact GitHub independently of your selected hub network route.

The stable update channel is [update-stable.json](https://raw.githubusercontent.com/fblah/android_control/main/update-stable.json). It contains signed metadata rather than an APK. No GitHub token should be entered into or bundled with the app.

## Replacing a development APK

The first production APK uses the permanent production signing identity. Android may refuse to replace a development APK signed with a different key. In that case, uninstall the development app, install this release and enroll the phone again. Uninstalling removes local enrollment and app data. Later production updates preserve the same signing identity and normally install over the existing production app.

## Current limitations

Use Safari on macOS for passkey setup if Brave’s Create passkey button appears unresponsive; the Brave issue is tracked for a later fix. Android may restrict background startup on some phones; force-stop and operating-system permissions still apply. Only grant access to a hub and administrators you trust.
