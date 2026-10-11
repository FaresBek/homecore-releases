HomeCore 0.1.4 adds device-aware automations with editable steps on the panel and web portal.

- Start from eight ideas, or create an automation from a device. Pickers search rooms, devices and controls.
- New triggers include attributes, sunrise/sunset offsets, intervals, button/events, availability and hub startup. Sun times are calculated locally using the hub location.
- Conditions include multiple states, attributes, sun windows, weekdays and nested and/or/not groups.
- Actions include device controls, wait-until, repeats, if/then/else, panel notices and enabling/disabling/running another automation.
- Run now executes actions only. Last-run results show success or the failed step. Existing saved automations remain compatible.

The panel and browser use shared capabilities and validation for sliders, options, device states and action parameters. Panel itself is unchanged.

IRU1 command events represent commands successfully sent by HomeCore. Physical handheld IR presses require a receiver that reports incoming events. Tuya/Sonoff repeated identical polls cannot establish another press without a changed event marker.

Production package: app.homecore. Version: 0.1.4. Android version code: 5. Signed with the existing HomeCore production certificate. Install over the existing production app to retain settings and devices.

Verified source: https://github.com/FaresBek/stips-panel/commit/4f534297d58c39f89f8cfe65b25041e07d981d05
PR and panel test instructions: https://github.com/FaresBek/stips-panel/pull/42

Validation: 446 Android unit tests, lint, debug/release builds, both branding checks, 19 Python checks and Chromium automation forms at 480×480 and 1280×800. The merged source tree matches the tested APK source exactly. Physical device behavior and Z4 resource use require on-device checks.
