Tuya QR login is now available directly in HomeCore without a Tuya developer account or cloud project. HomeCore retrieves account device keys, matches device IDs to LAN addresses, and keeps manual local-key entry available.

## Set up Tuya

1. Update HomeCore and open Integrations → Tuya LAN.
2. In Smart Life or Tuya Smart, open Me → Settings → Account and Security → User Code.
3. Enter that code in HomeCore, select the matching phone app, and show the QR.
4. Use + → Scan in that app and confirm login. Display the QR on the hub or another browser screen when using one phone.
5. Select the matched devices and add them. Devices must already belong to the authorized account.

For a device still marked Needs a key, select its checkbox and enter its 16-byte local key. Manual setup works without cloud sign-in. Refresh keys retrieves changed account keys for added devices.

The default QR connection uses Home Assistant's public Tuya sharing registration, following Tuya Local Key. The confirmation may identify Home Assistant. This relies on that registration and Tuya's service remaining available; custom client IDs and manual setup remain supported. Initial authorization and key refresh use the internet; device control uses the local network.

## Changes and validation

- Corrected the registration schema and Smart Life / Tuya Smart QR formats.
- Kept QR setup visible on desktop and phone browsers.
- Saved authorized registration with the encrypted session, including support for both endpoint spellings. Added-device keys remain after account sign-out.
- HomeCore 0.1.2, Android version code 3, production package app.homecore, signed with the same production key as 0.1.1.
- Android unit checks, Python tool checks, app lint/build and Chromium desktop/phone setup flows passed. A real Tuya account and physical devices still need testing on the hub's LAN.

Source: https://github.com/FaresBek/stips-panel/pull/40
Protocol references: https://github.com/vineetchoudhary/tuya-local-key and https://github.com/tuya/tuya-device-sharing-sdk
