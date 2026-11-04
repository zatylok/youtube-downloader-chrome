# Install VidoZavr 1.2.60

**[Русский](ru.md) · [English](en.md) · [Deutsch](de.md) · [Español](es.md) · [Português do Brasil](pt-BR.md)**

All functions are free. Use Windows 11 x64, Google Chrome 127+ and Internet for first
installation. The Windows Setup interface is Russian; these guides translate its labels.

## Recommended: Windows installer, then manual Chrome connection

[**Download VidoZavr.exe**](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr.exe)

Install Windows components, read the extension path on the final Setup page, then
load that exact folder from Chrome's **Load unpacked** action. The EXE already provides
the extension. **You do not need the ZIP as well.** Setup never opens Chrome.

Default folder: `%LOCALAPPDATA%\Programs\YouTube Video & Shorts Downloader\extension`.
Custom locations differ: the path on the final Setup page is authoritative.
Choose the folder containing `manifest.json`, not its parent or the ZIP.

## Other options

| Option | Download | Responsibilities |
|---|---|---|
| Advanced | [VidoZavr-Extension.zip](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr-Extension.zip) | Requires the Windows Native Host installed by the EXE. Extract into a permanent folder and maintain that independent copy manually. |
| **Beta/Experimental** | [VidoZavr-Experimental.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr-Experimental.exe) | Attempts automatic enrollment; profile selection, Developer mode, permission prompts or other extensions can prevent completion. Read the [limitations](EXPERIMENTAL.md). |

Both installers use the same identity and installation directory. Do not run both
at once or load duplicate extension copies. The public Experimental asset is named
`VidoZavr-Experimental.exe`; `experimental/` is only its local build subdirectory.

[Checksums](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/SHA256SUMS.txt) ·
[Components, exact sources and licenses](COMPONENTS.md) · [Main README](../../README.md)

## About the illustrations

The compact Russian and English control/card images are genuine **headless Chromium
149.0.7827.55** captures from disposable profiles, with numbered overlays on the controls.
The existing connection image is from the real extension and a verified isolated
Native response in headless Chromium 149. No Windows folder picker or Setup completion
image is simulated.

These images do not certify manual enrollment, Chrome 156 or a clean-Windows
installation. The card illustrations show the real extension/version, not a new
Native connection test. The original full controls image remains
[available](images/chrome-extensions.png).

The downloadable [documentation ZIP](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr-Documentation.zip)
remains the unchanged release-time snapshot, including license texts. These repository
guides receive documentation corrections without changing the release binaries.
