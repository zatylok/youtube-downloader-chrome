# VidoZavr 1.2.71 installieren

**[Русский](ru.md) | [English (US)](en.md) | [Français](fr.md) | [Deutsch](de.md) | [العربية](ar.md)**

Alle Funktionen sind kostenlos: YouTube-Videos, Shorts, Kanäle, Playlists, Livestreams,
Zuschneiden und Downloadverwaltung. Die Verarbeitung erfolgt auf Ihrem PC.
Sie benötigen **Windows 11 x64, Chrome 127+ und Internet bei der Erstinstallation**.
Python, Rust und Node.js sind nicht nötig. Die Windows-Komponente verbindet Chrome
über Native Messaging mit den lokalen Werkzeugen. **Die Erweiterung allein reicht nicht.**

Version 1.2.71 bietet einen gemeinsamen Editor für Videos und Shorts mit gespeicherten Entwürfen und bis zu acht zeitgesteuerten Masken. Die Entfernung nutzt lokale FFmpeg-Interpolation für feste, ungedrehte Rechtecke in 8-Bit-SDR. Auf komplexen Hintergründen können Spuren bleiben. Ein erfolgreicher Proxy-Test bestätigt die Verbindung. YouTube kann Metadaten trotzdem mit `bot_check` verweigern. Wählen Sie bei Bedarf manuell den Direktmodus.

## Empfohlene Installation: neun Schritte

1. **[VidoZavr.exe herunterladen](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/VidoZavr.exe).**
   Die zusätzliche ZIP ist nicht nötig. Nutzen Sie das offizielle Release und vergleichen
   Sie die [SHA-256-Prüfsumme](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/SHA256SUMS.txt).
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
8. **Eine aktivierte Karte V1D0Z@VR 🦖** mit Version **1.2.71** prüfen.
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

- **Eigenständige ZIP - [VidoZavr-Extension.zip](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/VidoZavr-Extension.zip)**
  Laden Sie nur dieses Archiv herunter, prüfen Sie den SHA-256-Wert und entpacken
  Sie alle Dateien in einen dauerhaften Ordner. Starten Sie **Установить компоненты.exe**
  (Windows-Komponenten installieren) mit Ihrem normalen Windows-Konto.
  Das Programm installiert den Native Host und fehlende geprüfte Werkzeuge.
  Folgen Sie danach den Schritten 4 bis 9 mit dem Ordner `extension` aus der ZIP,
  der `manifest.json` enthält. `Check.cmd` im Komponentenordner prüft Dateien
  und Registrierung.
- **Beta/Experimental - [VidoZavr-Experimental.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/VidoZavr-Experimental.exe):**
  versucht die automatische Einbindung mit derselben Windows-Installation.
  Entwicklermodus, Profilauswahl oder Berechtigungsentscheidungen können nötig sein;
  andere Erweiterungen können stören. Weder Erfolg noch unbeaufsichtigter Ablauf
  sind garantiert. Die Prüfung auf einem sauberen Windows ist unvollständig.
  Lesen Sie die [Einschränkungen](EXPERIMENTAL.md).

## Sicherheit und heruntergeladene Werkzeuge

Die EXEs haben **keine Windows-Authenticode-Signatur**. SmartScreen kann einen unbekannten
Herausgeber melden. Offizielle Quelle und Hash prüfen, im Zweifel abbrechen.
Schutzfunktionen nicht abschalten. Optionale Prüfung: `Get-FileHash .\VidoZavr.exe -Algorithm SHA256`.

Setup und der Komponenteninstaller der ZIP beziehen yt-dlp **2026.10.21**, Deno **2.9.8** und Gyan Doshis FFmpeg/FFprobe
**9.0.2** direkt von den festgelegten Anbietern und prüft Größe/SHA-256.
Diese Anbieter-EXEs sind nicht in unseren Downloads enthalten. Die Erstinstallation
ist nicht vollständig offline. [Komponenten, Quellen, Lizenzen und Hashes](COMPONENTS.md).
**Ed25519-signierte Programmupdates sind von der Windows-Installersignatur getrennt.**

## Aktualisieren und deinstallieren

**Standard- und Experimental-EXE.** Signierte Updates pflegen ihren verwalteten
Ordner und warten auf geschützte Aufgaben. Starten Sie zur Reparatur das passende
Setup erneut. Zeigt Chrome eine ältere Version, laden Sie die vorhandene Karte
in `chrome://extensions` und danach die YouTube-Tabs neu.

**ZIP-Installation.** Prüfen und entpacken Sie die neue offizielle ZIP getrennt.
Starten Sie nach Abschluss der Downloads `Установить компоненты.exe`. Ersetzen
Sie den vollständigen Ordner `extension` am bisherigen Pfad und laden Sie die
bestehende Karte und die Tabs neu. Beide Teile der ZIP werden manuell aktualisiert.
Zur Reparatur starten Sie den Komponenteninstaller erneut. Verwenden Sie bei einem
Konflikt das Verfahren der vorhandenen Installation.

Entfernen Sie Windows-Komponenten über **Windows-Einstellungen → Apps → V1D0Z@VR**.
Videos, `native\data`, `.updates` und der separat entpackte Erweiterungsordner
bleiben erhalten. Entfernen Sie die Chrome-Karte bei Bedarf manuell. Dabei können
lokale Einstellungen verloren gehen.

## Fehlerbehebung

| Problem | Unterstützte Vorgehensweise |
|---|---|
| Manifest fehlt / konnte nicht geladen werden | Erneut die entpackte Erweiterung laden und genau `extension` mit `manifest.json` auswählen. Downloads, der übergeordnete Ordner und die ZIP sind falsch. |
| Karte vorhanden, Downloader nicht verbunden | Windows-Komponente für **denselben Windows-Benutzer**, richtiges Chrome-Profil und genauen Ordner prüfen. `Check.cmd` im Programmordner prüft Dateien/Registrierung; das Erweiterungsmenü die aktive Verbindung. Zur Reparatur das passende Installationsprogramm ausführen. |
| Entwicklermodus aus | Im richtigen Profil einschalten, eingeschaltet lassen und die bestehende Karte aktivieren. |
| Falsches Profil oder doppelte Kopien | Das Profil der Installation und den beabsichtigten dauerhaften Ordner ermitteln. Keine weitere Kopie zur Verbindungsreparatur laden; das Entfernen einer Karte kann Einstellungen löschen. |
| Update beendet, Chrome-Version noch alt | Nach Ende geschützter Arbeit die **bestehende Karte** neu laden und YouTube-Tabs aktualisieren. Keine pausierten Daten löschen. |
| Netzwerk, VPN-Routen oder Download-/Hashfehler | Verbindung auch für den Downloader prüfen, nicht nur Chrome. Split-Tunneling kann unterschiedliche Routen bewirken. Offizielle Quelle erneut versuchen; keine fremden Spiegel, Hashänderungen oder abgeschalteten Schutzfunktionen. |
| SmartScreen-Warnung | Der Installer ist unsigniert. Quelle/Prüfsumme prüfen, im Zweifel abbrechen. |
| Experimental durch andere Erweiterung blockiert | Fremde Abfragen nicht blind bestätigen oder andere Erweiterungen deaktivieren. Eigenes Setup normal schließen und die empfohlene manuelle Installation nutzen. |

[Berechtigungen und Datenschutz](../../README.md#windows-warnings-permissions-and-privacy) ·
[Varianten und Sprachen](README.md)
