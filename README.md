# Winsense CS2 releases

This public repository is the download and update channel for Winsense CS2. The full project and build tools are kept in a separate private repository.

Download [the latest release](https://github.com/4479cantcode/winsense-cs2-releases/releases/latest) and run **WinsenseCS2Bootstrap.exe**. The launcher checks for updates each time it starts, verifies the downloaded package, installs it under your Windows user profile, and opens Winsense. If an update cannot finish, it offers Retry and Manual update.

Keep the launcher running while you use Winsense. It stays out of sight and checks CS2 when the game starts. If CS2 changes before a compatible Winsense release is ready, the launcher shows an update-coming-soon page with a retry option and a link to [discord.gg/4479](https://discord.gg/4479).

Each release contains:

| Asset | Use |
| --- | --- |
| `WinsenseCS2Bootstrap.exe` | Windows launcher and updater |
| `WinsenseCS2-<version>-win-x64.zip` | Core and packaged dashboard for manual installation |
| `manifest.json` | Version, minimum supported version, SHA-256 hashes, sizes, and changelog |

For a manual installation, extract the ZIP with its directory structure intact and start `WinsenseUI/WinsenseUI.exe`. The core sits at `x64/Release/Winsense.exe` relative to the extracted folder. The launcher is recommended because it verifies and installs updates automatically.

Release notes and older versions are on the [Releases page](https://github.com/4479cantcode/winsense-cs2-releases/releases). Human-readable changes are also in [CHANGELOG.md](CHANGELOG.md). Do not put API keys, private source, logs, or account data in this repository.
