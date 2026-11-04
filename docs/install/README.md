# VidoZavr 1.2.60 — installation

Installation options for the official VidoZavr 1.2.60 release.

| Option | Artifact | Who should use it |
|---|---|---|
| **Recommended** | `VidoZavr.exe` | Install Windows components, then manually load the installed extension folder in Chrome. Setup never opens Chrome. |
| Advanced | `VidoZavr-Extension.zip` plus the Windows installation | Use an independent unpacked folder only if you will maintain its files yourself. The ZIP alone is insufficient. |
| **Beta / Experimental** | `experimental/VidoZavr-Experimental.exe` | Try the existing automatic enrollment flow; Chrome actions or manual recovery may still be required. |

Both installers use the same application identity, Native Host and managed extension
directory. Choose one installer, not two separate installations. Do not load duplicate
extension copies. The experimental implementation and its tests remain maintained;
they are not part of the recommended installer's execution path.

- [Русский](ru.md)
- [English](en.md)
- [Deutsch](de.md)
- [Español](es.md)
- [Português do Brasil](pt-BR.md)
- [Exact components, downloads and licenses](COMPONENTS.md)
- [Experimental limitations](EXPERIMENTAL.md)

The release root supplies `SHA256SUMS.txt`, installer/ZIP sidecars, `LICENSE`,
`THIRD_PARTY_RU.txt` and notices. Screenshots, when included, are from isolated
headless Chromium with the real extension and Native Host. They illustrate controls;
they do not certify manual enrollment, a clean Windows guest or the owner's profile.
