# HomeCore releases

Signed Android production releases for HomeCore, with local smart-home integrations and its browser portal.

## Current release: 0.1.3

- [Download HomeCore 0.1.3 APK](https://github.com/FaresBek/homecore-releases/releases/download/v0.1.3/homecore-0.1.3-release.apk)
- [Release notes](https://github.com/FaresBek/homecore-releases/releases/tag/v0.1.3)
- [Update manifest](https://github.com/FaresBek/homecore-releases/releases/download/v0.1.3/homecore-release.json)

Android package: `app.homecore`. Android version code: `4`. This updates production 0.1.2 using the same package and signing certificate.

Tuya numeric controls and choices are editable using the device’s reported write permissions, ranges, steps and options. Read-only status values stay as sensors. Verified account mappings hide superseded raw DP rows. After updating, reload the browser portal and use Tuya **Refresh keys** for current names and control metadata.

**Settings > Integrations** opens setup directly. Enabled integration cards expand; disabled cards collapse. The portal keeps discoveries and progress current, preserves selected devices across live updates, and offers **Enter key** and **Add device** buttons beside discovered devices.

Tuya QR setup is available without a Tuya developer account or cloud project. Enter your Smart Life or Tuya Smart User Code, show a QR, scan and confirm in the selected app, then add devices whose account keys match their LAN addresses. The default uses Home Assistant's public Tuya sharing registration, as used by Tuya Local Key. Internet access is required for authorization and key refresh; commands use the LAN.

Tuya and Sonoff devices found on your network can also be added by selecting a device and entering its local key. The discovered ID and address are filled in automatically. Sonoff cloud login requires configured eWeLink application credentials.

The earlier `app.homecore.test` build remains a separate installation. Physical-device and account checks must be performed on the hub's local network.

## Updates and versioning

Use **Settings > Updates** in HomeCore to check this repository. Each `vX.Y.Z` release includes the signed APK and `homecore-release.json`, containing its package, version, SHA-256, size and source commit. HomeCore checks the APK against its pinned production signing certificate before installation.

HomeCore versions and Android version codes increase independently of the Panel app. Published versions are retained; corrections are released with a new version.

Source: [FaresBek/stips-panel](https://github.com/FaresBek/stips-panel). Source tags use `hub-vX.Y.Z`. See [release maintenance instructions](https://github.com/FaresBek/stips-panel/blob/main/docs/HOMECORE_RELEASING.md) for version bump commands and the signing/publishing workflow.

The release repository publisher verifies the APK in `release/` against its manifest, production package and pinned signing certificate, then publishes both assets using GitHub's repository token. Published versions cannot be replaced, and both version numbers must increase. It uses an already-signed APK and never handles the private signing key.

No signing keystore, passwords or device local keys belong in this public repository.
