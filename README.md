# V1D0Z@VR 🦖 / VidoZavr

**100% Free / Полностью бесплатно**

Download YouTube videos, Shorts, channels, playlists and LIVE, with cropping and
download management directly on YouTube. Media processing runs on your Windows PC.

Скачивайте видео YouTube, Shorts, каналы, плейлисты и трансляции прямо на YouTube.
Обрезка и управление загрузками включены. Все функции бесплатны, без подписки и PRO.

## [Download VidoZavr.exe — recommended / Скачать — рекомендуется](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr.exe)

**Windows 11 x64 · Google Chrome 127+ · Internet for installation**  
**[Русский](docs/install/ru.md) · [English](docs/install/en.md) · [Deutsch](docs/install/de.md) · [Español](docs/install/es.md) · [Português do Brasil](docs/install/pt-BR.md)**

Advanced: [Extension ZIP](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr-Extension.zip) ·
Optional: [Automatic installer — Beta/Experimental](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr-Experimental.exe) ·
[SHA-256 checksums](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/SHA256SUMS.txt)

## Choose one installation route / Выберите один вариант

| Option | What to do |
|---|---|
| **Recommended — [VidoZavr.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr.exe)** | Install Windows components, then connect the installed folder to Chrome manually. **No separate ZIP needed.** / Установите EXE и вручную подключите папку расширения. ZIP не нужен. |
| Advanced — [VidoZavr-Extension.zip](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr-Extension.zip) | Extract into a permanent folder. **The Windows Native Host is still required**; install it with the recommended EXE. Update the independent folder manually. / Без Windows-компонента ZIP не работает. |
| Optional — [VidoZavr-Experimental.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr-Experimental.exe), **Beta/Experimental** | Attempts automatic Chrome enrollment. Developer mode, profile selection or permission decisions may be needed; other extensions can block it. Success is not guaranteed. / Автоподключение может потребовать ваших действий или завершиться неудачей. |

Both installers use the same identity and directory. Choose one; do not load duplicate
extension copies. [Experimental limitations](docs/install/EXPERIMENTAL.md) include
incomplete clean-Windows verification.

## Recommended setup in a few steps

1. Download and run **VidoZavr.exe**. Setup installs Windows components; it does not open Chrome.
2. On the final Russian Setup page, find the exact **extension folder**.
   **Папка расширения** means “Extension folder”; **Инструкция** means “Instructions”.
3. Open `chrome://extensions` in your YouTube Chrome profile. Turn on
   **Developer mode**, then click **Load unpacked**.
4. In the folder picker, select the **exact installed `extension` directory containing
   `manifest.json`**, not Downloads, the parent installation folder or the ZIP.
5. Check the **V1D0Z@VR 🦖** card. Open it from Chrome's puzzle-piece menu and confirm
   **Downloader connected** / **Загрузчик подключён**.

Default extension location:

`%LOCALAPPDATA%\Programs\YouTube Video & Shorts Downloader\extension`

**Use the path shown by Setup if you chose a different location.** Keep this folder
and Developer mode enabled. The [illustrated English guide](docs/install/en.md) and
[пошаговая инструкция на русском](docs/install/ru.md) cover every step and common errors.
Setup is Russian; the guides are available in five languages.

## Why Windows components and Internet are needed

Chrome supplies the YouTube controls. The Windows Native Messaging host runs local
download tools and communicates with the extension. **The ZIP alone cannot download.**
No Python, Rust, Node.js, manual registry editing or administrator elevation is required.

Our installers and application updates **do not bundle vendor EXEs**. Setup downloads
missing, pinned tools directly from their providers and checks sizes and SHA-256:

| Tool | Purpose | Pinned version / provider |
|---|---|---|
| yt-dlp | Retrieve YouTube media | 2026.10.21 / yt-dlp GitHub Releases |
| Deno | YouTube JavaScript and the application-update controller | 2.9.8 / Deno GitHub Releases |
| FFmpeg / FFprobe | Process media and check video/audio | 9.0.2 / Gyan Doshi Windows build |

Existing tools with the required hashes can be reused. First installation is not
fully offline. [Exact URLs, hashes, licenses and components](docs/install/COMPONENTS.md)
are documented separately.

## Windows warnings, permissions and privacy

The installers are **not Windows Authenticode-signed**. SmartScreen may show an unknown
publisher. Check the official source and [SHA-256](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/SHA256SUMS.txt);
cancel if uncertain. Do not disable antivirus, SmartScreen or Chrome security.
**Ed25519-signed application updates are a separate protection**, not Windows EXE signing.

The extension uses Native Messaging for the local host, storage for preferences/history,
activeTab and scripting for YouTube controls, and alarms for update checks. It accesses
supported YouTube pages and Return YouTube Dislike for dislike counts. Its manifest
is included in the extension ZIP. Stable ID: `bkihgeeibbodemeibfdcglojjkiepnlf`.

Media processing and task records stay on your PC. Downloads contact YouTube/CDNs;
dislike requests send the video ID to Return YouTube Dislike without credentials;
updates contact GitHub and tool acquisition contacts the listed vendors.
The downloader does not import browser cookies/accounts. Local processing does not
mean offline operation or certified anonymity. Read Chrome permission requests yourself.

## Updates and removal

Signed application updates verify the official repository, Ed25519 signature and file
inventory, and wait while protected media work remains. They maintain the installed
extension folder. If Chrome still shows an older version, reload **the existing card**
and refresh YouTube tabs; do not remove it for a routine update. An independent ZIP
folder must be updated manually from the matching official ZIP.

Repair with the recommended Setup after downloads finish. If it reports busy files,
follow its message; never delete paused downloads or partials to force an update.
Uninstall through **Windows Settings → Apps → V1D0Z@VR**, then remove the Chrome card.
Downloaded media, `native\data` and `.updates` are retained. Removing the Chrome card
can remove its browser-local settings. The guides cover [troubleshooting](docs/install/en.md#troubleshooting).

## Help, author projects and optional support

[GitHub Issues](https://github.com/zatylok/youtube-downloader-chrome/issues) ·
[Developer @zatylok007](https://t.me/zatylok007)  
Include your version, the error and brief reproduction steps; omit cookies, tokens,
personal browser profiles and private history.

Author projects: [Food Swipe](https://foodswipe.ru) ·
[Currency/crypto Telegram bot](https://t.me/KursyValutNowBot)  
[Coffee and cat treats](https://donatr.ee/zatylok) are voluntary. **Every function stays free.**

Original project code: [MIT](LICENSE). Vendor and bundled-library licenses remain
separate; see [components and attribution](docs/install/COMPONENTS.md).
Not affiliated with YouTube or Google.

[Latest official release](https://github.com/zatylok/youtube-downloader-chrome/releases/latest) ·
[All installation guides](docs/install/README.md)
