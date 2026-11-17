# Your phone, made easier

Use the matching hub 0.6.0-dev or newer and the latest signed APK. A normal update keeps your existing enrollment and passkeys.

## On the phone

- **Home** shows whether setup is needed, approval is pending, the connection is starting/reconnecting, or access is paused. **Pause all access** stops remote access and ringing. **Resume access** enables it again.
- **Files** shows incoming files and connected computers you can send a selected file to. **Save to phone…** opens Android’s destination picker. Files remain limited to 10 MiB; full folder browsing is not available yet.
- **Sharing** contains location, notification and phone-finder permissions, remote-lock setup and connected-computer permissions.
- **Settings** contains phone name, network preference, hub setup and app updates.

## Distinguish your devices

On each phone/tablet, open Settings, enter a recognizable name (such as Personal phone, Work phone or Home tablet), then **Save phone name**. In the browser, choose it from **Current device** at the top. Status, transfers, notifications, location and controls follow that selection. The administrator can select devices across family accounts; members see their own devices.

## Keep it running when closed

Once a hub is trusted, the connection runs separately from the app screen. Swiping away the app should leave it running. After a restart, unlock the phone once and allow networking to reconnect; you should not need to open Android Control. Home → **Review background settings** explains Android’s Unrestricted/background/Auto-start settings. Tailscale must reconnect too if using Tailscale-only mode.

An explicit pause stays paused after restart. Android **Force stop**, revoked permissions and manufacturer battery restrictions can prevent background operation; reopen the app if needed. Real restart behavior must be tested on each device.

## Ring the selected phone or tablet

In the browser choose **Start ringing**, then **Stop ringing**. You can also stop it on the phone or from its notification. Sound stops automatically within one minute. It uses the current alarm volume and respects Android sound restrictions; it does not turn the volume up or bypass Do Not Disturb. Pausing access and revoked/expired controller access stop ringing too.

## Enable location from your computer

Choose **Turn on location sharing**. To allow this without another phone approval, first enable **Allow computer to enable location** on the phone and grant Android’s required location permissions. Otherwise the browser tells you to approve on the phone, and a phone notification is shown where permitted.

This cannot silently grant Android permissions or switch on Android’s GPS setting. Turning location sharing off on the phone also removes remote-enable consent. See [location history and privacy](LOCATION.md).

## Lock and unlock

On the phone, choose Sharing → **Set up remote lock** and approve Android’s device administrator request. The browser can then **Lock phone**. Have the phone’s normal PIN/password available; Android may require it for the next unlock. You can remove this permission from Sharing.

**Ask phone to unlock** sends a notification to that phone. Tap it and use **Unlock with Android**. Android still verifies the normal PIN/password/fingerprint. This feature never bypasses a secured screen or gives the browser your PIN. If request notifications are blocked, unlock the phone normally.
