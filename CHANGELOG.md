# Changelog

## v1.0.1

- The launcher checks CS2 compatibility when the game starts and watches for later game launches while Winsense runs.
- If game offsets have changed, it checks for a newer release. When none exists, it shows an update-coming-soon page with retry and a Discord link.
- Keeps the v1.0.0 working core and dashboard while adding the compatibility check to the launcher.

## v1.0.0

- First CS2 distribution through a dedicated public GitHub Releases channel.
- Added a launcher that checks for updates on startup, verifies release hashes, and installs versions side by side.
- Added an update-required screen with retry and manual download options.
- Packaged the existing working CS2 core and dashboard as the initial baseline.
