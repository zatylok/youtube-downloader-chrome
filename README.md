# V1D0Z@VR 🦖 — VidoZavr 1.2.60

Free YouTube downloads and video tools directly on YouTube: videos, Shorts, channels,
playlists, LIVE, cropping and download management. Media processing runs locally.
Author support is optional; there are no paid features or subscriptions.

**All functions are free.** No PRO subscription, paywall or mandatory donation.
Version 1.2.60 improves safe download recovery and first-activation Shorts auto-scroll.

## Download and installation

Use the [latest official release](https://github.com/zatylok/youtube-downloader-chrome/releases/latest).
Windows 11 x64 and Chrome 127+ are required. Choose one installation route:

[**Download VidoZavr.exe**](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr.exe) ·
[Extension ZIP](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr-Extension.zip) ·
[Experimental installer](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr-Experimental.exe) ·
[SHA-256 checksums](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/SHA256SUMS.txt)

| Route | File | Behavior |
|---|---|---|
| **Recommended** | **VidoZavr.exe** | Installs Windows components and the managed extension folder. Never opens or controls Chrome. Connect the extension manually. |
| Advanced | VidoZavr-Extension.zip plus Windows components | An independent unpacked extension copy. Its files require manual updates. |
| **Beta / Experimental** | VidoZavr-Experimental.exe | Preserved automatic Chrome enrollment. It may require Developer mode, permission decisions or manual recovery; success is not guaranteed. |

Both installers use the same application identity and directory. Do not install two
separate copies or load duplicate extensions. The Experimental option has observed
profile/other-extension limitations and incomplete clean-Windows verification.
Read its [limitations](docs/install/EXPERIMENTAL.md) before choosing it.

Recommended steps:

1. Verify the installer hash, run VidoZavr.exe and finish the Windows installation.
2. Open `chrome://extensions` in the intended Chrome profile.
3. Enable **Developer mode**, select **Load unpacked**, then select the installed
   `extension` directory shown by Setup. `manifest.json` must be at that directory's root.
4. Open V1D0Z@VR and check **Downloader connected**, or the equivalent in its selected language.

The default extension directory is
`%LOCALAPPDATA%\Programs\YouTube Video & Shorts Downloader\extension`.
The final Setup page shows the exact path if you selected another location.
The EXE already supplies this extension: the ZIP is not another required download.

Complete guides: [Русский](docs/install/ru.md) · [English](docs/install/en.md) ·
[Deutsch](docs/install/de.md) · [Español](docs/install/es.md) ·
[Português do Brasil](docs/install/pt-BR.md).

## Why a Windows EXE is required

Chrome uses a small Rust Native Messaging host to communicate with local media tools.
The ZIP alone cannot download media. Setup installs that host, its configuration,
the extension, local installation/update scripts and required notices; it registers
the host for the current Windows user. No manual registry editing, administrator
elevation, Python, Rust or Node.js installation is required. Setup is not a Windows service.

The recommended installer verifies Windows files and registration. It does **not**
claim that you have connected Chrome or that live Native Messaging was tested.

## Internet downloads and exact providers

Our EXE and application-update assets do not bundle the four vendor executables.
If missing, Setup obtains these pinned packages via HTTPS and checks their exact
sizes and SHA-256 before installing them:

| Component | Version | Upstream | Actual distribution provider |
|---|---|---|---|
| yt-dlp | 2026.10.21 | [yt-dlp](https://github.com/yt-dlp/yt-dlp) | [yt-dlp GitHub Release EXE](https://github.com/yt-dlp/yt-dlp/releases/download/2026.10.21/yt-dlp.exe) |
| Deno | 2.9.8 | [Deno](https://github.com/denoland/deno) | [Deno GitHub Release ZIP](https://github.com/denoland/deno/releases/download/v2.9.8/deno-x86_64-pc-windows-msvc.zip) |
| FFmpeg / FFprobe | 9.0.2 | [FFmpeg](https://ffmpeg.org/) | [Gyan Doshi essentials ZIP](https://github.com/GyanD/codexffmpeg/releases/download/9.0.2/ffmpeg-9.0.2-essentials_build.zip) |

Verified tools already installed can be reused. First installation is not fully offline.
Application updates come separately from authenticated releases in this VidoZavr repository.
Vendor maintenance uses the pinned vendor catalog, not arbitrary latest versions.
The [component audit](docs/install/COMPONENTS.md) gives exact byte sizes, archive and
executable hashes, provider/upstream distinctions, bundled components, destinations
and failure behavior.

## SHA-256 and Windows warnings

Compare files with `SHA256SUMS.txt` and their `.sha256` sidecars from the same release.
For example, `Get-FileHash .\VidoZavr.exe -Algorithm SHA256` is a read-only check.

The Windows installers currently **lack Authenticode signing**. Windows SmartScreen
may report an unknown publisher. Verify source and hash; cancel if uncertain.
Do not disable antivirus, SmartScreen or Chrome security. Ed25519 signing of
application updates is a distinct mechanism and does not make the EXE Windows-signed.

## Chrome permissions

Keep Developer mode enabled for the unpacked extension. The stable extension ID is
`bkihgeeibbodemeibfdcglojjkiepnlf`; its Native Messaging host is
`com.local.shorts_downloader`.

| Permission / access | Purpose |
|---|---|
| `nativeMessaging` | Communicate with the installed local downloader. |
| `storage`, `unlimitedStorage` | Persist preferences and the download-list UI, including larger histories. |
| `activeTab`, `scripting` | Work with the current supported page and restore content scripts. |
| `alarms` | Schedule application/vendor status checks. |
| YouTube desktop/mobile hosts | Inject download controls and support YouTube navigation and tools. |
| `returnyoutubedislikeapi.com/votes*` | Request dislike counts for a video ID. |

Read any Chrome approval yourself. Neither installer is a browser security bypass.

## Privacy and local processing

Media files and task state are processed and stored on your PC. Downloads contact
YouTube and its media CDN. The dislike feature requests the video ID from Return
YouTube Dislike with credentials omitted. Update checks contact GitHub; dependency
acquisition contacts the providers above. Those services receive normal network requests.
The downloader's current media command disables importing browser cookies/accounts.
This is not an independent certification of no telemetry, universal anonymity,
antivirus approval or complete offline operation.

## Updating and uninstalling

Signed application updates maintain the managed installation directory, check
Ed25519, repository identity and file inventory, and defer while protected work remains.
If Chrome still displays the old version, reload the existing extension card and
refresh YouTube tabs. Seamless activation across all Chrome builds is not promised.
An independently extracted ZIP folder needs matching replacement files and a manual
card reload; Setup does not maintain it.

Run Setup again to repair the Windows installation after work finishes. If files are
busy, the guard may require temporarily disabling the extension; do not delete paused
tasks or partial files to force an update. Uninstall using Windows Settings → Apps →
V1D0Z@VR, then remove the Chrome card. Downloaded media, `native\data` and `.updates`
are retained; removing the Chrome card can remove its browser-local preferences.

## Troubleshooting and licensing

Report reproducible bugs through [GitHub Issues](https://github.com/zatylok/youtube-downloader-chrome/issues)
or the existing developer contact [@zatylok007](https://t.me/zatylok007). Include the
version and short reproduction steps; omit browser profiles, cookies, tokens and private history.

Author projects: [Food Swipe](https://foodswipe.ru) and the
[currency/crypto Telegram bot](https://t.me/KursyValutNowBot).
[Optional coffee and cat-treat support](https://donatr.ee/zatylok) never unlocks features;
all functions remain free.

For connection errors, verify the same Windows user, the installed Windows component,
and the exact unpacked folder. `Check.cmd` checks local files/registration; the popup
shows the live connection. Network/hash failures must be retried from the official
source without changing pins or substituting mirrors. Split-tunnel VPNs can route
Chrome and the downloader differently.

The project's original code uses [MIT](LICENSE). Vendor binaries and bundled libraries
retain their own licenses. yt-dlp's Windows bundle is GPLv3+ with separate notices;
Deno is MIT with V8/other notices; the selected Gyan static FFmpeg build is GPLv3,
including external libraries. The installer includes Inno Setup/Pascal Script/LZMA
and Rust dependency notices. See [component attribution](docs/install/COMPONENTS.md)
and the release `licenses` directory. We do not claim that the entire combined
dependency stack has one license or that vendor repackaging source obligations
have been satisfied by a link alone. Not affiliated with YouTube or Google.

Development-only tools and publisher secrets are not included in the installation.
