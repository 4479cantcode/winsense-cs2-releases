# Changelog

## v1.0.5

- Fixed the HUD radar and bomb overlay failing to appear. The overlay window was created once and never rebuilt when it resized to the game window, so anything drawn outside the stale backbuffer was clipped away. It now rebuilds its swap chain on every resize.
- Reworked the 2D tactical radar: range rings, a view cone, off-radar enemies that clamp to the edge instead of disappearing, health rings, a planted-bomb marker with site and countdown, and no more collision with the other HUD panels.
- Reworked the bomb HUD: it now uses the bomb's real timer length instead of assuming 40 seconds, shows a proper site badge, a defuse countdown, and escalates from white to amber to a pulsing red in the final ten seconds.
- Bunny hop now writes the usercmd jump button directly. The old injected keypress had to land inside a one-tick window and be delivered to the foreground thread, which it usually was not.
- Topmost now re-asserts itself, so the overlay stays above the game after fullscreen switches and focus changes instead of silently dropping behind it.
- The overlay FPS cap and entity snapshot rate now default to maximum, and a setting of 0 genuinely means uncapped as the label claims.
- Dashboard live trends are now individual cards with a title above each graph, current value, min/avg/max, hover readout, and pause and clear controls. A new snapshot-cost chart was added.
- The dashboard status bar now shows a live bomb timer and ping instead of entity count and IPC state, and the runtime health panel no longer reports false failures while CS2 is closed.
- Added a Discord button that opens the community invite, a collapsible language selector that sits beside it, and a theme dropdown with circle previews and four new palettes.
- The dashboard now launches the newest core build instead of the first one it finds on disk, which is what caused earlier fixes to appear missing.
- Everything now reports 1.0.5.

## v1.0.4

- Unified the version number across the app, the core and the release channel. Everything now reports 1.0.4.
- The dashboard no longer shows 2.0.0, and the core licence report no longer sends 2.0.1. Both now send 1.0.4, so the dashboard, the website and the admin diagnostics view agree with the release version.
- Includes the current tested core, dashboard, and launcher.

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
