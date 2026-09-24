# Changelog

## v1.0.8

- Refreshed CS2 build 14183 offsets and verified all embedded values against the current dumper.
- Rebuilt match timing and dashboard telemetry for accurate round number, round timer, phase, ping, entity count, and live snapshot health.
- Added draggable, lockable, and resizable HUD panels. Positions, widths, and lock state now persist per config.
- Expanded radar sizing from 32 to 1000 pixels and added resize grips to the radar and six HUD panels.
- Redesigned the dashboard around per-tab presets and moved advanced controls into focused presets.
- Added compact narrow-window layouts, a smaller key screen and minimum window size, interface scaling, synchronized dashboard topmost controls, and custom in-panel scrollbars.
- Added default-value markers to sliders and inline numeric entry by clicking the displayed value.
- Improved overlay reliability, topmost behavior, secondary-monitor support, uncapped FPS pacing, snapshot latency, and device-loss recovery.
- Fixed ESP text sizing, FOV defaults and world/viewmodel updates, snaplines, team-color behavior, knives, bomb-carrier filtering, crouched head height, and glove finishes.
- Fixed aimbot smoothing and autofire timing, triggerbot hold/burst behavior, movement edge cases, damage-log totals, and round-number fallbacks.
- Hardened licence expiry handling, saved-key verification, transient failure behavior, IPC reconnects, config loading, and UI crash recovery.
- Added four dashboard themes and improved skin, grenade-helper, match, spectator, damage, watermark, keybind, and player-list panels.

## v1.0.6

- Fixed the launcher wrongly reporting "CS2 update coming soon" on current game builds. The build-number sanity window was 10,000-100,000, but CS2 passed 1,000,000, so every current build was rejected as incompatible even when the offsets matched exactly.
- A CS2 build that has not populated its global variables yet, such as the main menu or between rounds, is now treated as still loading and retried instead of being called incompatible.
- Updated every embedded CS2 offset to the current dump. All 143 embedded values now match.
- The dashboard now reports the live overlay state: above the game, hidden, or behind the game, and warns when the game appears to be running exclusive fullscreen, where no overlay can sit on top.
- Redesigned the launcher loading and update screens with clearer hierarchy, a live download percentage, a stage line describing the current step, and a version chip.
- Replaced the launcher Discord button with a Discord icon in both the loading and update screens.
- Launcher updated to 1.2.0. Everything else now reports 1.0.6.

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
