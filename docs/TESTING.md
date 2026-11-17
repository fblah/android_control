# Test the new app and controls

After updating both the hub and APK, test on each phone and tablet:

1. Set a distinct name in the phone’s Settings and save it. Switch Current device in the browser and confirm that controls and displayed data belong to that device.
2. Start/stop ringing. Only the selected device should ring. Try the phone’s Stop ringing control too, then check the one-minute automatic stop.
3. Swipe the phone app out of recent apps. Without reopening it, request status and ring from the browser.
4. Restart the phone, unlock it once, leave Android Control closed and wait roughly a minute for networking. Try status and ringing. Review background/Auto-start settings if it does not reconnect.
5. Test location while locked. With optional background history enabled, allow about 20 minutes with some movement and check fix timestamps/accuracy. Saved history should remain visible after a fresh browser login while the phone is offline.
6. Test remote location enablement with and without the phone’s prior consent. Missing Android permissions must lead to phone approval, not a silent grant.
7. Enable remote lock on the phone and lock it from the browser. Ask it to unlock; normal phone authentication must still be required. Remove remote-lock permission and check that new lock requests ask for setup.
8. Pause all access while ringing. Sound must stop and new requests must fail. Restart while paused; it must stay paused until you resume on the phone. Existing history may remain visible, but there should be no new fix timestamps.
9. Transfer a small file both ways. Incoming files should appear on Files, and Save to phone should ask where to save. Canceling the picker must not save anything.

Do not use Android Force stop for the ordinary close-app test: it deliberately blocks application execution. Keep real coordinates, setup QR codes, credentials and private notifications out of public issues. When reporting a failure, include the device/Android version, step number and message shown.
