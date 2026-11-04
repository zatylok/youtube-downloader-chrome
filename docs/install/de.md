# VidoZavr 1.2.60 installieren

**[Русский](ru.md) | [English (US)](en.md) | [Français](fr.md) | [Deutsch](de.md) | [العربية](ar.md)**

Alle Funktionen sind kostenlos: YouTube-Videos, Shorts, Kanäle, Playlists, Livestreams,
Zuschneiden und Downloadverwaltung. Die Verarbeitung erfolgt auf Ihrem PC.
Sie benötigen **Windows 11 x64, Chrome 127+ und Internet bei der Erstinstallation**.
Python, Rust und Node.js sind nicht nötig. Die Windows-Komponente verbindet Chrome
über Native Messaging mit den lokalen Werkzeugen. **Die Erweiterung allein reicht nicht.**

## Empfohlene Installation: neun Schritte

1. **[VidoZavr.exe herunterladen](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr.exe).**
   Die zusätzliche ZIP ist nicht nötig. Nutzen Sie das offizielle Release und vergleichen
   Sie die [SHA-256-Prüfsumme](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/SHA256SUMS.txt).
2. **Die EXE starten und die Windows-Komponenten installieren.** Setup ist russisch:
   **Далее = Weiter**, **Готово = Fertigstellen**. Warten Sie auf **Компоненты Windows
   установлены** (Windows-Komponenten installiert). Fehlende festgelegte Werkzeuge
   werden heruntergeladen und geprüft; passende geprüfte Dateien werden wiederverwendet.
   Setup öffnet Chrome nicht und prüft keine aktive Browserverbindung.
3. **Die letzte Setup-Seite vor dem Schließen lesen.** Das Pfadfeld zeigt den dauerhaften
   Erweiterungsordner. **Папка расширения = Erweiterungsordner** öffnet ihn;
   **Инструкция = Anleitung** öffnet die installierte Anleitung. Den genauen Pfad für Schritt 7 merken.
4. **`chrome://extensions`** im Chrome-Profil öffnen, das Sie für YouTube verwenden.
   Geben Sie die Adresse in die Adressleiste ein; dies ist eine interne Seite, keine Website.
5. Rechts oben den **Entwicklermodus** einschalten.
6. **Entpackte Erweiterung laden** anklicken. Die Windows-Ordnerauswahl öffnet sich.
7. **Genau den installierten Ordner `extension` aus Schritt 3 auswählen.**
   Navigieren Sie dorthin oder fügen Sie den genauen Setup-Pfad in das Feld **Ordner**
   ein und bestätigen Sie mit **Ordner auswählen** (russisches Windows: **Папка**,
   **Выбор папки**). `manifest.json` muss direkt darin liegen. Wählen Sie den Ordner,
   nicht die Datei, „Downloads“, den übergeordneten Installationsordner oder eine ZIP.
8. **Eine aktivierte Karte V1D0Z@VR 🦖** mit Version **1.2.60** prüfen.
   Im Entwicklermodus lautet die ID `bkihgeeibbodemeibfdcglojjkiepnlf`.
9. **Chrome-Puzzlemenü „Erweiterungen“ → V1D0Z@VR** öffnen.
   Prüfen Sie **Downloader verbunden** (russisch: **Загрузчик подключён**).
   Bei Bedarf das Symbol anheften. Eine Karte allein belegt noch keine Native-Verbindung.

Standardordner:

`%LOCALAPPDATA%\Programs\YouTube Video & Shorts Downloader\extension`

**Bei einer benutzerdefinierten Installation kann der Pfad abweichen. Maßgeblich ist
der genaue Pfad auf der letzten Setup-Seite.** Behalten Sie den dauerhaften Ordner
und lassen Sie den Entwicklermodus eingeschaltet. Nach dem Schließen von Setup finden
Sie die Anleitung im Startmenü; verwenden Sie den gewählten Installationsordner und
dessen Unterordner `extension`.

### Die Bedienelemente

Die Aufnahme zeigt die **englische** Oberfläche: **1 Developer mode = Entwicklermodus**,
**2 Load unpacked = Entpackte Erweiterung laden**. Echter Headless-Chromium 149,
ohne die ungenutzte Fläche.

![Englische Bedienelemente mit den Nummern 1 und 2](images/chrome-controls-en.png)

Die echte Erweiterungskarte zeigt Namen, Version, ID und aktivierten Schalter.

![VidoZavr-Karte in englischem Chromium](images/extension-card-en.png)

<details>
<summary>Beispiel einer bestätigten Verbindung (russische Oberfläche)</summary>

**1** markiert „Загрузчик подключён“ / „Downloader verbunden“. Die vorhandene Aufnahme
zeigt eine echte isolierte Native-Antwort, keinen neuen manuellen Installationstest.

![Bestätigte Native-Verbindung im Erweiterungsmenü](images/connected.png)

</details>

Die Bilder stammen aus isoliertem **Headless-Chromium 149**, nicht Chrome 156 oder
einem frisch installierten Windows. Die Karte dient der Veranschaulichung; die
[ursprüngliche Gesamtansicht](images/chrome-extensions.png) bleibt verfügbar.
Setup-Abschluss und Windows-Ordnerauswahl werden nicht durch nachgebildete Bilder dargestellt.

## Weitere Installationswege

- **Für Fortgeschrittene — [VidoZavr-Extension.zip](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr-Extension.zip):**
  Die Windows-Komponente mit der empfohlenen EXE installieren, die ZIP in einen eigenen
  dauerhaften Ordner entpacken und diesen **statt** der verwalteten Kopie laden.
  Chrome lädt keine ZIP direkt. Setup und signierte Updates pflegen diesen unabhängigen
  Ordner nicht: Dateien mit der passenden offiziellen ZIP ersetzen und die bestehende
  Karte neu laden. Nicht beide Kopien laden.
- **Beta/Experimental — [VidoZavr-Experimental.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr-Experimental.exe):**
  versucht die automatische Einbindung mit derselben Windows-Installation.
  Entwicklermodus, Profilauswahl oder Berechtigungsentscheidungen können nötig sein;
  andere Erweiterungen können stören. Weder Erfolg noch unbeaufsichtigter Ablauf
  sind garantiert. Die Prüfung auf einem sauberen Windows ist unvollständig.
  Lesen Sie die [Einschränkungen](EXPERIMENTAL.md).

## Sicherheit und heruntergeladene Werkzeuge

Die EXEs haben **keine Windows-Authenticode-Signatur**. SmartScreen kann einen unbekannten
Herausgeber melden. Offizielle Quelle und Hash prüfen, im Zweifel abbrechen.
Schutzfunktionen nicht abschalten. Optionale Prüfung: `Get-FileHash .\VidoZavr.exe -Algorithm SHA256`.

Setup bezieht yt-dlp **2026.10.21**, Deno **2.9.8** und Gyan Doshis FFmpeg/FFprobe
**9.0.2** direkt von den festgelegten Anbietern und prüft Größe/SHA-256.
Diese Anbieter-EXEs sind nicht in unseren Downloads enthalten. Die Erstinstallation
ist nicht vollständig offline. [Komponenten, Quellen, Lizenzen und Hashes](COMPONENTS.md).
**Ed25519-signierte Programmupdates sind von der Windows-Installersignatur getrennt.**

## Aktualisieren und deinstallieren

Signierte Programmupdates pflegen den installierten Ordner und warten, solange geschützte
Medienaufgaben bestehen. Zeigt Chrome danach eine alte Version, auf der bestehenden
Karte unter `chrome://extensions` **Neu laden** wählen und YouTube-Tabs aktualisieren.
Karte und Einstellungen behalten; eine nahtlose Aktivierung wird nicht für jede
Chrome-Version zugesichert. Unabhängige ZIP-Ordner erfordern manuelle Dateiupdates.

Zur Reparatur Setup nach Arbeitsende erneut ausführen und Meldungen zu belegten Dateien
befolgen. Pausierte Aufgaben und Teildateien erhalten. Deinstallation: **Windows-Einstellungen →
Apps → V1D0Z@VR → Deinstallieren**, danach die Chrome-Karte entfernen.
Videos, `native\data` und `.updates` bleiben erhalten. Das Entfernen der Karte kann
ihre im Browser gespeicherten Einstellungen löschen.

## Fehlerbehebung

| Problem | Unterstützte Vorgehensweise |
|---|---|
| Manifest fehlt / konnte nicht geladen werden | Erneut die entpackte Erweiterung laden und genau `extension` mit `manifest.json` auswählen. Downloads, der übergeordnete Ordner und die ZIP sind falsch. |
| Karte vorhanden, Downloader nicht verbunden | Windows-Komponente für **denselben Windows-Benutzer**, richtiges Chrome-Profil und genauen Ordner prüfen. `Check.cmd` im Programmordner prüft Dateien/Registrierung; das Erweiterungsmenü die aktive Verbindung. Bei Bedarf nach Arbeitsende mit Setup reparieren. |
| Entwicklermodus aus | Im richtigen Profil einschalten, eingeschaltet lassen und die bestehende Karte aktivieren. |
| Falsches Profil oder doppelte Kopien | Das Profil der Installation und den beabsichtigten dauerhaften Ordner ermitteln. Keine weitere Kopie zur Verbindungsreparatur laden; das Entfernen einer Karte kann Einstellungen löschen. |
| Update beendet, Chrome-Version noch alt | Nach Ende geschützter Arbeit die **bestehende Karte** neu laden und YouTube-Tabs aktualisieren. Keine pausierten Daten löschen. |
| Netzwerk, VPN-Routen oder Download-/Hashfehler | Verbindung auch für den Downloader prüfen, nicht nur Chrome. Split-Tunneling kann unterschiedliche Routen bewirken. Offizielle Quelle erneut versuchen; keine fremden Spiegel, Hashänderungen oder abgeschalteten Schutzfunktionen. |
| SmartScreen-Warnung | Der Installer ist unsigniert. Quelle/Prüfsumme prüfen, im Zweifel abbrechen. |
| Experimental durch andere Erweiterung blockiert | Fremde Abfragen nicht blind bestätigen oder andere Erweiterungen deaktivieren. Eigenes Setup normal schließen und die empfohlene manuelle Installation nutzen. |

Hilfe: [GitHub Issues](https://github.com/zatylok/youtube-downloader-chrome/issues) oder
[@zatylok007](https://t.me/zatylok007). Version, genaue Meldung und kurze Schritte nennen;
keine Cookies, Tokens oder privaten Profile senden.
[Berechtigungen und Datenschutz](../../README.md#windows-warnings-permissions-and-privacy) ·
[Varianten und Sprachen](README.md)
