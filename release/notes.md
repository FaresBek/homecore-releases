HomeCore 0.1.3 adds editable Tuya controls and improves integration setup in the app and browser portal.

- Writable numeric data points use sliders with the device's range, step and unit; writable enum data points use dropdowns. Presence, illuminance and other read-only values remain sensors.
- Verified cloud mappings hide old duplicate/offline DP rows and unrecognized raw fields. Numeric and choice commands are validated before being sent locally.
- Settings opens Integrations directly. Enabled cards expand; disabled cards collapse.
- The portal at your hub's IP:8080 keeps discovered devices current without resetting selections. Use Enter key or Add device beside a device; fetching and adding show progress.
- Tuya QR login still retrieves keys and matches device IDs to LAN addresses automatically. Manual local-key setup remains available.

After updating, reload the browser portal. For existing Tuya devices, use Integrations → Tuya LAN → Refresh keys to retrieve the latest names, permissions and control limits. Devices must be reachable from the hub's local network. If a dashboard references a retired raw sensor DP, select its replacement editable entity.

Production package: app.homecore. Version: 0.1.3. Android version code: 4. Signed with the same production certificate as earlier HomeCore releases; install over your existing production app.

Validation includes Android unit tests/lint/builds, portal regression tests, Home Assistant editor compatibility, release identity/branding checks, and Chromium tests at desktop and phone sizes. Device commands still need verification on the installer's physical LAN.
