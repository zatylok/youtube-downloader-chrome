# Automatic installer — Beta / Experimental, 1.2.60

**The recommended installer is VidoZavr.exe with manual Chrome enrollment.**
`experimental/VidoZavr-Experimental.exe` is the separate automatic-enrollment option.
It uses the same extension ID, Native Host, installation directory and signed-update
mechanism; do not treat it as a second application or load duplicate extension copies.

The existing implementation is preserved in `installer/YouTubeDownloader.iss` and
`installer/resources/ChromeEnrollment.ps1`. Its focused and isolated GUI tests remain
available. An explicit `--experimental` build selects it; the default selects the
Windows-only `installer/YouTubeDownloader-Manual.iss` instead. No enrollment algorithm
was rewritten for this packaging change.

This option may open a dedicated Chrome window, ask for a Chrome profile, require
you to enable Developer mode and wait for Chrome permission decisions. It never
legitimately bypasses those decisions. Other extensions, including observed CAdES
and McAfee prompts, can block it. Clean-Windows verification remains **NOT VERIFIED**.
Earlier isolated Chrome 156 tests passed initial enrollment, a real Native response
and normal restart, but repeat enrollment was blocked by an unrelated CAdES prompt.

On the owner's PC, the prior r2 helper was observed waiting at a hidden profile-choice
form before it created a Chrome marker window. That path has no dialog deadline.
This remains a known limitation of the preserved experimental implementation, not a
claim that the recommended manual installer follows that path. Do not describe the
experimental option as guaranteed, fully unattended or generally qualified.

If it stalls, use the standard installer and the [manual guide](en.md). Do not change
Chrome policies, unrelated extensions or security software to force automation.
Do not launch both installers concurrently. If Windows reports files in use, close
your own Setup normally and finish protected work before retrying; do not discard data.
