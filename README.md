# CatchCraze config

Public, read-only settings the game fetches at start-up. The game's source is elsewhere and private.

`version.json`, per platform:

- `min_version`: below this version the game asks the player to update and does not open.
- `latest_version`: below this version the game suggests an update the player can skip.

Versions are the App Store version (e.g. `1.2`), not build numbers. The game only blocks when the
store really offers a version at least as new, so raise `min_version` only after the update is live.

`ios_testflight` is for testing on a phone before a version is in the store. It is read only by
TestFlight installs, and only when `store_version` is set: that version stands in for the App Store's,
and UPDATE opens TestFlight. Leave `store_version` empty when not testing.

Never put secrets here: everyone can read this file.
