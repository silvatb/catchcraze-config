# CatchCraze config

Public, read-only settings the game fetches at start-up. The game's source is elsewhere and private.

`version.json`, per platform:

- `min_version`: below this version the game asks the player to update and does not open.
- `latest_version`: below this version the game suggests an update the player can skip.

Versions are the App Store version (e.g. `1.2`), not build numbers. The game only blocks when the
store really offers a version at least as new, so raise `min_version` only after the update is live.

Never put secrets here: everyone can read this file.
