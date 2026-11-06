# VidoZavr 1.2.62 - components, downloads and integrity

## In plain language

The extension adds controls to YouTube. A small Windows component runs the downloads
and media processing on your PC, which Chrome cannot do alone. Setup installs our
application and obtains three verified packages: yt-dlp retrieves media, Deno handles
YouTube JavaScript and the update controller, and FFmpeg/FFprobe process and check
video and audio. You do not install Python, Rust or Node.js yourself.

First installation needs Internet access. The three vendor packages total about
168 MiB; their exact providers, versions and hashes are below. Application updates
and vendor tools are separate downloads. Neither Windows installer is Authenticode-signed;
Ed25519 authenticates application updates, not the Windows installer.

Interface languages and maintained guides: [Русский](ru.md) | [English (US)](en.md) |
[Français](fr.md) | [Deutsch](de.md) | [العربية](ar.md). The Windows installer remains Russian.

[Installation guides](README.md) ·
[Pinned dependency catalog](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.62/online-dependencies.json) ·
[Notices and license texts](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.62/VidoZavr-Documentation.zip)

The documentation ZIP is the unchanged release-time snapshot. The guides on the
repository's `main` branch are maintained separately. References to `licenses/...`
below identify files in that ZIP and the installation, not missing repository pages.

## Technical reference

This is an audit of the pinned 1.2.62 build, not a list of current upstream versions.
The machine-readable catalog is supplied as `online-dependencies.json` in the release
and installation. All four tools below are required by this build; they are not optional
plugins. The optional items are the independent extension ZIP, Experimental installer
and voluntary author support.

## Inside our installer

`VidoZavr.exe` contains the Chrome extension, the Rust Native Host
`native/shorts-native.exe`, first-party installation/update scripts, pinned compatibility
catalogs, public publisher/extension identity, instructions and license notices.
The Native EXE includes its compiled Rust libraries; notices are in `licenses/rust`.
It does not embed Python as a separately installed runtime or install Node.js/Rust.

The installer shell is Inno Setup 7.1.0 with Pascal Script and LZMA compression;
the applicable notices are `Inno-Setup-LICENSE.txt`, `Pascal-Script-LICENSE.md` and
`LZMA-SDK.txt` in the release `licenses` directory. Extended 7-Zip archive DLLs are
not included; vendor ZIP extraction uses Windows .NET `System.IO.Compression`.

Windows PowerShell 5.1 and the Windows .NET Framework run the installation scripts;
they are existing Windows components, not additional package downloads. Windows
Shell/Explorer is used only for explicit folder/document actions. The Experimental
variant additionally uses Windows UI Automation and Windows Forms. Google Chrome
is installed separately by the user; the recommended Setup neither downloads nor starts it.

**yt-dlp.exe, deno.exe, ffmpeg.exe and ffprobe.exe are not embedded in either of our
installer variants, the extension ZIP or our signed application-update payload.**
The Experimental variant additionally embeds the existing Chrome enrollment helper.
Neither variant includes signing secrets, browser profiles or user media.

## Downloaded during installation when missing

Pinned archive sizes are exact bytes; downloaded and extracted files are checked
against the catalog before installation or execution. Downloads use HTTPS from the
exact initial URL, allowing only the same original URL or GitHub's
`release-assets.githubusercontent.com` delivery host on redirects.

| Package | Purpose | Version | Download bytes | Archive SHA-256 |
|---|---|---|---:|---|
| yt-dlp | YouTube metadata and media acquisition | 2026.10.21 | 17,880,111 | `33121d192d706e62f684a06f80918e3f3a8ba52ac3a65213b6951c39c7d9f555` |
| Deno ZIP | YouTube JavaScript challenges and the local application-update controller | 2.9.8 | 42,917,472 | `cba84b26e0df5ae7f74fc66b86a95b866872a86292ebd84fa1e959927edd93bf` |
| FFmpeg essentials ZIP | Merge/process media and validate output with FFprobe | 9.0.2 | 114,768,076 | `60f467265b1e312373dbcd92200c2618a74850f98d3d078e94296bb3fa2047ba` |

The three downloads total **175,565,659 bytes** when all are needed. Existing installed
tools with the exact pinned size/hash can be reused; a repair need not redownload them.
An authenticated developer QA cache is a test facility, not a promise that the consumer
EXE is an offline installer. The vendor archive can contain files not installed by
VidoZavr; only the catalog's exact four executable entries are extracted.

### Exact sources and providers

- **yt-dlp:** [upstream project](https://github.com/yt-dlp/yt-dlp).
  Provider: the project's GitHub Releases, initial domain `github.com`.
  Actual URL: [yt-dlp.exe, 2026.10.21](https://github.com/yt-dlp/yt-dlp/releases/download/2026.10.21/yt-dlp.exe).
  The Windows standalone executable bundles its Python/runtime dependencies; yt-dlp's
  source is Unlicense, while its combined Windows executable is GPLv3+ with separate
  notices. Bundled `yt-dlp-ejs` 0.8.0 is used locally; remote component downloads are
  disabled by this application. See [upstream licensing](https://github.com/yt-dlp/yt-dlp#license),
  `licenses/yt-dlp-THIRD_PARTY_LICENSES.txt` and `licenses/EJS-LICENSE`.
- **Deno:** [upstream project](https://github.com/denoland/deno).
  Provider: Deno's GitHub Releases, initial domain `github.com`.
  Actual URL: [Deno Windows x64 ZIP, v2.9.8](https://github.com/denoland/deno/releases/download/v2.9.8/deno-x86_64-pc-windows-msvc.zip).
  Deno is MIT; bundled V8 and other dependencies retain their own notices.
  See [Deno license](https://github.com/denoland/deno/blob/main/LICENSE.md),
  `licenses/Deno-LICENSE.md` and `licenses/V8-LICENSE`.
- **FFmpeg/FFprobe:** [upstream project](https://ffmpeg.org/),
  **distribution provider Gyan Doshi**, not an FFmpeg-project Windows build.
  Actual URL: [Gyan 9.0.2 essentials ZIP](https://github.com/GyanD/codexffmpeg/releases/download/9.0.2/ffmpeg-9.0.2-essentials_build.zip),
  initial domain `github.com`, provider repository `GyanD/codexffmpeg`.
  The lockfile retains the earlier Gyan convenience URL
  `https://www.gyan.dev/ffmpeg/builds/ffmpeg-release-essentials.zip`; the **installer
  actually uses the versioned GitHub URL above**, bound to the same approved hash.
  This is a static GPLv3 essentials build including external libraries such as libx264,
  not an LGPL-only build. See [Gyan's build information](https://www.gyan.dev/ffmpeg/builds/),
  [FFmpeg licensing](https://ffmpeg.org/legal.html), `licenses/FFmpeg-LICENSE`,
  `licenses/FFmpeg-README.txt` and `licenses/FFmpeg-BUILDCONF.txt`.
  The [official FFmpeg source mirror](https://github.com/FFmpeg/FFmpeg) and
  [license text](https://github.com/FFmpeg/FFmpeg/blob/master/COPYING.GPLv3)
  are also available on GitHub if the informational website is unreachable.

Keep the corresponding notices and copyright attributions with redistributed material.
The project's original code is MIT; that does not relicense vendor binaries or their
bundled libraries. Repackaging vendor binaries requires separately addressing their
applicable notices/source obligations. We do not claim a complete corresponding-source
bundle for repackaged vendor EXEs; these release assets do not redistribute those EXEs.

### Installed executable inventory

Paths are relative to the chosen installation directory, normally
`%LOCALAPPDATA%\Programs\YouTube Video & Shorts Downloader`.

| Installed file | Bytes | SHA-256 |
|---|---:|---|
| `native/bin/yt-dlp.exe` | 17,880,111 | `33121d192d706e62f684a06f80918e3f3a8ba52ac3a65213b6951c39c7d9f555` |
| `native/bin/deno.exe` | 98,081,568 | `924397800533d3eb0ed0c889b20ad70e18b970d93acd8135bc043f425e528266` |
| `native/bin/ffmpeg.exe` | 105,423,872 | `3256173f3f8bffd7df12227c68adf68025edb1832273a9530688a7bb1ed8edec` |
| `native/bin/ffprobe.exe` | 105,221,120 | `f0d36ecbbdd3bcfac3efa078c96c7271c2e68b3810595552ac3b7f17e9a65c52` |

## Later downloads and failures

Application updates use the official
[VidoZavr repository](https://github.com/zatylok/youtube-downloader-chrome), immutable
repository ID `1430910943`. The client requests repository/release metadata from
`api.github.com`, then `v1d0zvr-update.json` and hash-named `.bin` assets from that
repository's ordinary releases on `github.com`/`release-assets.githubusercontent.com`.
It validates the Ed25519 envelope, repository binding, inventory, sizes and SHA-256,
waits for protected media work, and uses the existing transactional updater/rollback.
It never accepts an unsigned local draft as a production update.

Vendor maintenance is separate: checks compare the approved catalog; repair obtains
only missing/mismatched pinned tools from the vendor URLs above. It does not download
arbitrary `latest` executables or plugin packages. The update controller may make a
verified **local copy** of Deno in its protected per-installation update cache; this
is not another external download.

The downloader contacts YouTube and its media CDN for requested content. The dislike
feature contacts `returnyoutubedislikeapi.com/votes` with the video ID; its requests
omit credentials. GitHub and dependency providers also see their normal network
requests. This documentation does not assert an independently certified absence of
all telemetry or universal offline operation.

Network failure, unexpected redirect, size mismatch or SHA-256 mismatch refuses the
component before use. Required-tool failure prevents completion and shows a Russian
error with Retry/Cancel; valid installed data is not discarded. Initial acquisition
has bounded transport attempts. Do not use alternate mirrors, alter expected hashes
or disable security to force an install. Browser connectivity does not prove that a
separate native process has the same route, especially with split-tunnel VPNs.
