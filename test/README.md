HomeCore 0.1.4 (version code 5), signed with the existing HomeCore production certificate for manual testing.

Built from FaresBek/stips-panel commit 514d597255bfe41fbedd00ab6a6c0e0d2c62ecee, PR #42:
https://github.com/FaresBek/stips-panel/pull/42

- New device-aware triggers, conditions and actions, including sun, events, availability, waits, repeats and if/else.
- Eight starter ideas and editable panel/web forms with shared capabilities and validation.
- Location settings, panel notices, actions-only Run now and last-run results.
- Existing automations remain compatible; Panel is unchanged.

CI passed, including tests, lint, both apps' builds and both HomeCore branding checks:
https://github.com/FaresBek/stips-panel/actions/runs/38133250470

IRU1 events currently represent commands sent by HomeCore. Incoming handheld IR presses require an event-reporting receiver.

This is a pre-release for manual installation. The current production update remains 0.1.3.
