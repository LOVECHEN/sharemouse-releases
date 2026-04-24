# ShareMouse Releases Mirror

[中文说明](README_CN.md)

Automated mirror of [ShareMouse](https://www.sharemouse.com/) official releases.

## How It Works

- **Daily check** (08:00 UTC) via GitHub Actions, also supports manual trigger
- Scrapes the official download page and changelog for the latest Windows & macOS versions
- Downloads installers and portable archives, computes SHA-256 checksums
- Publishes GitHub Releases with platform-specific changelogs and file verification data
- Windows and macOS versions are tracked **independently** — if both reach the same version number, assets are merged into a single release

## Assets Per Release

| Platform | Files |
|----------|-------|
| 🪟 Windows | `ShareMouseSetup.exe`, `ShareMouse_USB.zip` |
| 🍎 macOS | `ShareMouseSetup.dmg`, `ShareMouseMac.zip` |

## Links

- 📥 [Official Download Page](https://www.sharemouse.com/download/)
- 📋 [Windows Changelog](https://www.sharemouse.com/download/changelog/)
- 📋 [macOS Changelog](https://www.sharemouse.com/download/changelog-mac/)
