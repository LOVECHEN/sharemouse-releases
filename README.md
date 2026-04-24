# ShareMouse Releases Mirror

Automated daily mirror of [ShareMouse](https://www.sharemouse.com/) official releases (Windows + macOS).

## How it works

A GitHub Actions workflow runs daily at **08:00 UTC** to:

1. Scrape the [official download page](https://www.sharemouse.com/download/) for the current version
2. Compare against the latest GitHub Release tag in this repo
3. If a new version is detected:
   - Download all official installers (Win EXE, Win Portable ZIP, Mac DMG, Mac Portable ZIP)
   - Compute **SHA-256** checksums and file sizes
   - Scrape the **changelog** for the current version only (both [Windows](https://www.sharemouse.com/download/changelog/) and [Mac](https://www.sharemouse.com/download/changelog-mac/))
   - Create a new **GitHub Release** named after the version number
   - Upload all files as release assets

## Release Contents

Each release includes:

| File | Description |
|------|-------------|
| `ShareMouseSetup.exe` | Windows Installer |
| `ShareMouse_USB.zip` | Windows Portable Edition |
| `ShareMouseSetup.dmg` | macOS Installer |
| `ShareMouseMac.zip` | macOS Portable Edition |

SHA-256 checksums and file sizes are listed in the release notes.

## Manual Trigger

You can also trigger the workflow manually from the **Actions** tab → **Check ShareMouse Updates** → **Run workflow**.

## License

This repository only mirrors publicly available downloads from [sharemouse.com](https://www.sharemouse.com/). ShareMouse is a product of [Bartels Media GmbH](https://www.bartelsmedia.com/).
