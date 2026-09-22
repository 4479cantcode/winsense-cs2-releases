# Changelog

## v1.0.3

- Adds CS2 session logging to the 4479 licence service, matching the Roblox external.
- While a licence is active, the core reports session start, a heartbeat every 60 seconds, and exit, with the device ID, client version and your linked 4479 account. The server records the IP address it sees.
- Licence keys are never sent in session logs, and logging problems never block a valid licence.
- Includes the current tested core, dashboard, and launcher.

## v1.0.2

- Updated the CS2 dashboard and account experience.
- Keeps the verified automatic updater and current offset compatibility checks.
- Includes the latest tested core and dashboard distribution build.

## v1.0.1

- The launcher checks CS2 compatibility when the game starts and watches for later game launches while Winsense runs.
- If game offsets have changed, it checks for a newer release. When none exists, it shows an update-coming-soon page with retry and a Discord link.
- Keeps the v1.0.0 working core and dashboard while adding the compatibility check to the launcher.

## v1.0.0

- First CS2 distribution through a dedicated public GitHub Releases channel.
- Added a launcher that checks for updates on startup, verifies release hashes, and installs versions side by side.
- Added an update-required screen with retry and manual download options.
- Packaged the existing working CS2 core and dashboard as the initial baseline.
