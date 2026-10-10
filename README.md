# HomeCore releases

Signed Android production releases for HomeCore, with local smart-home integrations and its browser portal.

## Current release: 0.1.1

- [Download HomeCore 0.1.1 APK](https://github.com/FaresBek/homecore-releases/releases/download/v0.1.1/homecore-0.1.1-release.apk)
- [Release notes](https://github.com/FaresBek/homecore-releases/releases/tag/v0.1.1)
- [Update manifest](https://github.com/FaresBek/homecore-releases/releases/download/v0.1.1/homecore-release.json)

Android package: `app.homecore`. Android version code: `2`.

This production package installs alongside the earlier `app.homecore.test` build. Android treats them as separate apps. Future production updates use the same package and signing certificate.

Tuya and Sonoff devices found on your network can be added by selecting a device and entering its local key. The discovered ID and address are filled in automatically. Vendor developer credentials are only needed for the supported cloud account setup routes.

The IR integration includes a fix for duplicate entity IDs, and Settings sections load independently with retry controls.

## Updates and versioning

Use **Settings > Updates** in HomeCore to check this repository. Each `vX.Y.Z` release includes the signed APK and `homecore-release.json`, containing its package, version, SHA-256, size and source commit. HomeCore checks the APK against its pinned production signing certificate before installation.

HomeCore versions and Android version codes increase independently of the Panel app. Published versions are retained; corrections are released with a new version.

Source: [FaresBek/stips-panel](https://github.com/FaresBek/stips-panel). Source tags use `hub-vX.Y.Z`. See [release maintenance instructions](https://github.com/FaresBek/stips-panel/blob/main/docs/HOMECORE_RELEASING.md) for version bump commands and the signing/publishing workflow.

No signing keystore, passwords or device local keys belong in this public repository.
