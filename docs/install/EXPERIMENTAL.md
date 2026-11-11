# Automatic installer - Beta/Experimental, 1.2.71

**For most users, choose [VidoZavr.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/VidoZavr.exe)
and the [manual Chrome guide](en.md). The separate ZIP is not required.**

[Download VidoZavr-Experimental.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/VidoZavr-Experimental.exe)
only if you want to try automatic Chrome enrollment.

The public filename has no subdirectory. In the local build output it is stored as
`experimental/VidoZavr-Experimental.exe`; that is not a public download URL.
Both installers use the same extension ID, Windows Native Host, installation directory
and signed updates. This is an alternative installer, not a second application.
Do not run both concurrently or load duplicate extension copies. If the standalone
ZIP components are already installed, follow the ZIP update and removal steps in the guides.

## What may require your attention

- Chrome may ask you to choose a profile or enable **Developer mode**.
- You must read and decide Chrome permission requests yourself.
- Other extensions can interrupt the flow. CAdES and McAfee prompts have been observed;
  VidoZavr should not accept, disable or dismiss them for you.
- Profile selection can stall. A prior helper waited at a hidden profile-choice form
  with no dialog deadline; the final Experimental variant preserves that implementation.

Earlier isolated Chrome 156 tests verified initial enrollment, a genuine Native
response and normal restart. Repeated enrollment was also blocked by an unrelated
CAdES prompt. **Clean-Windows verification is incomplete.** The installer is not
guaranteed or fully unattended, and those earlier results do not prove success on
every profile or PC.

## If it does not finish

Close your own Setup normally and use the recommended installer with the
[manual instructions](en.md). If Windows reports files in use, finish protected
downloads and follow its message before retrying. Preserve paused tasks and partials.

Do not change Chrome policies, disable security or interfere with unrelated extensions
to force enrollment. A third-party warning should be handled by its owner, not by
blind automation.

[Русский](ru.md) | [English (US)](en.md) | [Français](fr.md) | [Deutsch](de.md) | [العربية](ar.md)
