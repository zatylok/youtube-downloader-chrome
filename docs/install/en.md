# Install VidoZavr 1.2.71

**[Русский](ru.md) | [English (US)](en.md) | [Français](fr.md) | [Deutsch](de.md) | [العربية](ar.md)**

All functions are free: YouTube videos, Shorts, channels, playlists, LIVE, cropping
and download management. Processing runs locally. Use **Windows 11 x64, Chrome 127+
and Internet for first installation**. No Python, Rust or Node.js is needed.
The Windows component connects Chrome to the local download tools through Native
Messaging; **the extension alone is not enough**.

Version 1.2.71 brings one editor to regular videos and Shorts, with saved drafts and up to eight timed masks. Eraser uses local FFmpeg interpolation for stationary, unrotated rectangles on 8-bit SDR video. Complex backgrounds can show artifacts. A successful proxy test confirms connectivity. YouTube can still refuse metadata with `bot_check`. Select Direct manually when appropriate.

## Recommended installation: nine steps

1. **Download [VidoZavr.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/VidoZavr.exe).**
   You do not need the extension ZIP as well. Use the official release and compare
   its [SHA-256](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/SHA256SUMS.txt).
2. **Run the EXE and install Windows components.** Setup is Russian: **Далее = Next**,
   **Готово = Finish**. Wait for **Компоненты Windows установлены** (Windows components
   installed). Missing pinned tools are downloaded and checked; verified installed
   tools can be reused. Setup does not open Chrome or test a live browser connection.
3. **Read the final Setup page before closing it.** Its path field gives the permanent
   extension directory. **Папка расширения = Extension folder** opens that folder;
   **Инструкция = Instructions** opens the installed guide. Keep the exact path for step 7.
4. **Open `chrome://extensions`** in the Chrome profile you use for YouTube.
   Type this into Chrome's address bar; it is an internal page, not a website.
5. **Turn on Developer mode** at the top right.
6. **Click Load unpacked.** Chrome opens a Windows folder picker.
7. **Select the exact installed `extension` folder from step 3.**
   Navigate to it in the picker, or paste the exact Setup path into its **Folder**
   field and choose **Select Folder** (Russian Windows: **Папка**, **Выбор папки**).
   The selected folder must contain `manifest.json` directly. Select the folder,
   not the manifest file, Downloads, the parent installation directory or a ZIP.
8. **Confirm one enabled V1D0Z@VR 🦖 card**, version **1.2.71**.
   With Developer mode on, its ID is `bkihgeeibbodemeibfdcglojjkiepnlf`.
9. **Open Chrome's puzzle-piece Extensions menu → V1D0Z@VR.**
   Check **Downloader connected** (Russian: **Загрузчик подключён**).
   You may pin its icon for easier access. A card alone does not prove the Native connection.

Default directory:

`%LOCALAPPDATA%\Programs\YouTube Video & Shorts Downloader\extension`

**A custom installation path can differ. The expanded path shown by Setup is authoritative.**
Keep that permanent folder and Developer mode enabled. If you closed Setup, the
Start-menu installation guide gives the manual connection instructions; use your
chosen installation directory, then its `extension` subfolder.

### What the controls look like

**1** Developer mode · **2** Load unpacked. Genuine English headless Chromium 149;
the unused area is excluded from the capture.

![English Extensions controls, numbered 1 and 2](images/chrome-controls-en.png)

The real extension card below shows its name, version, ID and enabled switch.

![VidoZavr extension card in English Chromium](images/extension-card-en.png)

<details>
<summary>Connection confirmation example (Russian interface)</summary>

**1** marks “Загрузчик подключён” / “Downloader connected”. This existing image shows
a real isolated Native response, not a new manual-enrollment test.

![Verified Native connection in the real extension popup](images/connected.png)

</details>

Screenshots are from disposable **headless Chromium 149**, not Chrome 156 or a fresh
Windows installation. The card is a controlled illustration; the original full
[Extensions view](images/chrome-extensions.png) is retained. No Setup completion or
Windows picker screenshot is being simulated.

## Other installation options

- **Standalone ZIP - [VidoZavr-Extension.zip](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/VidoZavr-Extension.zip):**
  Download only this archive, verify its SHA-256, and extract all files to a permanent
  folder. Run the included **Установить компоненты.exe** (Install Windows components)
  as your regular Windows user. It installs the Native Host and missing verified tools.
  After Windows components are ready, follow steps 4-9 with the ZIP's `extension`
  folder containing `manifest.json`. Use the extracted folder for Chrome.
  `Check.cmd` in the Windows components folder verifies files and registration.
- **Beta/Experimental - [VidoZavr-Experimental.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/VidoZavr-Experimental.exe):**
  attempts automatic enrollment using the same Windows installation. Developer mode,
  profile selection or permission decisions may be needed; other extensions may
  interrupt it. It is not guaranteed or fully unattended. Clean-Windows verification
  is incomplete. Read the [limitations](EXPERIMENTAL.md).

## Security and downloaded tools

The EXEs are **not Windows Authenticode-signed**; SmartScreen may show an unknown
publisher. Check the official source/hash and cancel if uncertain. Never disable
security to force installation. Optional check: `Get-FileHash .\VidoZavr.exe -Algorithm SHA256`.

Setup and the ZIP component installer obtain yt-dlp **2026.10.21**, Deno **2.9.8**, and Gyan Doshi's FFmpeg/FFprobe
**9.0.2** directly from their pinned providers, with size/SHA-256 checks. Those vendor
EXEs are not bundled in our downloads. First installation is not fully offline.
[Components, providers, licenses and exact hashes](COMPONENTS.md) explain the details.
**Ed25519-signed application updates are separate from Windows installer signing.**

## Updates and uninstall

**Standard and Experimental EXEs.** Signed updates maintain their managed folder
and wait for protected media work. Rerun the respective Setup for repair.
If Chrome still shows an old version, reload the existing card in
`chrome://extensions` and refresh YouTube tabs.

**ZIP installation.** Verify and extract the new official ZIP separately. After
protected work finishes, run its `Установить компоненты.exe`. Replace the complete
`extension` folder at its existing path, then reload the current card and tabs.
Both parts of the ZIP update manually. Rerun the component installer for repair.
If a different installation already exists, use its own update or removal procedure.

Remove Windows components for any option in **Windows Settings → Apps → V1D0Z@VR**.
Downloaded media, `native\data`, `.updates`, and the separately extracted extension
remain. Remove the Chrome card manually if desired. This may erase its preferences.

## Troubleshooting

| Problem | Supported action |
|---|---|
| “Manifest missing” / “Could not load manifest” | Repeat **Load unpacked** and select the exact `extension` folder containing `manifest.json`. Downloads, its parent and a ZIP are wrong targets. |
| Card exists, downloader disconnected | Check the Windows component is installed for the **same Windows user**, the correct Chrome profile and exact folder. `Check.cmd` in the installation checks files/registration; the popup checks the live connection. For repair, rerun the installer for your installation method. |
| Developer mode is off | Enable it in the intended profile, keep it on, and check that the existing card is enabled. |
| Wrong profile or duplicate copies | Switch to the profile where you loaded VidoZavr and identify the intended permanent folder. Do not add another copy to fix a connection; removing a card may erase its preferences. |
| Update finished, Chrome still shows the old version | After protected work finishes, reload the **existing card**, then refresh YouTube tabs. Do not delete paused data. |
| Network, VPN routing or tool-download/hash failure | Check connectivity for the downloader as well as Chrome. Split tunneling can route them differently. Retry the official source; do not substitute mirrors, alter hashes or disable security. |
| SmartScreen warning | The installer is unsigned. Verify its official source/checksum; cancel if uncertain. |
| Experimental blocked by another extension | Do not accept unrelated prompts blindly or disable other extensions. Close your Setup normally and use the recommended manual route. |

[Permissions and privacy](../../README.md#windows-warnings-permissions-and-privacy) ·
[Options and languages](README.md)
