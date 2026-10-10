HomeCore 0.1.1 (Android version code 2)

- Select a Tuya or Sonoff device found on your network to enter its local key and add it. The device ID and IP are filled in automatically.
- Settings loads core controls, HomeKit and activity separately, with a retry action for a failed section. A failed request while the portal is live no longer claims the hub is unreachable.
- Fixed the IR integration SQLite UNIQUE constraint crash caused by colliding remote/button names, preserving existing dashboard targets and user names.
- Native IRU1 setup imports devices, rooms and saved TV/AC remotes through your IR account.
- Simplified eWeLink account setup and Tuya project import can retrieve keys and match local addresses when the required vendor credentials are configured.
- Production releases now use independent HomeCore semantic versions, increasing Android version codes and the pinned HomeCore signing certificate.

Production package: app.homecore. Install this APK alongside the earlier app.homecore.test build. Cloud login still requires the appropriate vendor developer credentials; adding LAN devices with an existing local key does not.

The APK is signed with the supplied keycore production key. Future updates are checked through Settings > Updates using the accompanying homecore-release.json manifest.
