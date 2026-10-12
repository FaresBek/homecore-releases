HomeCore 0.1.5 fixes main-hub setup and restart on Android 10 screens, including the Android version listed for Z4 and P1008.

The registry used database UPSERT syntax unavailable in Android 10's SQLite 3.22. Saving Main hub mode could crash during integration registration, then repeat the crash on every launch. Registry writes now use compatible transactions.

Install this APK over the existing HomeCore app to retain the installer PIN, hub mode, devices, rooms and automations. If setup was interrupted, choose Main hub and enter the saved PIN to finish it. No data reset or database migration is required.

- Integration, discovery, device and entity updates preserve stable IDs, links, installer overrides, disabled/ignored choices and original timestamps.
- Tests reproduce the old syntax failure and exercise older SQLite explicitly, including rollback after a rejected foreign-key update.
- Panel and existing automation/control behavior are unchanged.

Production package: app.homecore. Version: 0.1.5. Android version code: 6. Signed with the existing production certificate.

Fix details: https://github.com/FaresBek/stips-panel/pull/43
Validation includes registry/app tests, lint, builds, both branding checks and production certificate/alignment checks. Physical panels were not attached to the build workspace.
