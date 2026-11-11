**V1D0Z@VR 1.2.71 🦖** - бесплатное расширение Chrome для загрузок и редактирования прямо на YouTube. Все функции бесплатны. Обработка медиа выполняется на вашем Windows-ПК.

## Скачать и установить

| Вариант | Для кого |
|---|---|
| **[VidoZavr.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/VidoZavr.exe)** | **Рекомендуется.** Установите компоненты Windows, затем вручную подключите указанную Setup папку в Chrome. Дополнительный ZIP не нужен. |
| [Автономный ZIP](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/VidoZavr-Extension.zip) | Распакуйте в постоянную папку. Запустите вложенный `Установить компоненты.exe`, затем отдельно загрузите папку `extension` из ZIP. Обе части обновляются вручную. |
| [Beta/Experimental](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/VidoZavr-Experimental.exe) | Пробует подключить Chrome автоматически. Возможны режим разработчика, выбор профиля и запросы разрешений. Успех не гарантируется. |

Для ручного подключения откройте `chrome://extensions`, включите режим разработчика и нажмите «Загрузить распакованное расширение». Выберите именно папку `extension` с `manifest.json`. Нужны Windows 11 x64, Chrome 127+ и интернет при первой установке.

[Русский](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.71/docs/install/ru.md) | [English (US)](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.71/docs/install/en.md) | [Français](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.71/docs/install/fr.md) | [Deutsch](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.71/docs/install/de.md) | [العربية](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.71/docs/install/ar.md)

## Новое в 1.2.71

- Быстрее обработка обычных временных отрезков: убраны лишние декодирующие проверки.
- Исправлено ненужное перекодирование, когда начало совпадает с ключевым кадром, а конец находится внутри последнего кадра. Выбранные кадры и исходное качество сохраняются.
- Исправлены папки для отредактированных Shorts и отрезков обычного видео.
- Улучшена проверка скопированных пакетов, FPS и времени. Журнал различает копирование, кодирование и проверку.

[**Посмотреть интерфейс и примеры редактора**](https://github.com/zatylok/youtube-downloader-chrome/tree/v1.2.71#как-выглядит-vidozavr)

По-прежнему доступны видео, Shorts, каналы, плейлисты, LIVE с доступного начала, единый редактор с обрезкой по времени и кадру, восемь масок, поворот, «Удаление ✨», черновики, возобновление, десять одновременных загрузок, прокси и история обновлений. Качество просмотра и скачивания выбирается отдельно. Сейчас поддерживается YouTube; другие платформы планируются.

## Важно

- Исходное качество может давать большие файлы. Для меньшего доступного исходника явно выберите «До 1080p» или «До 720p» в редакторе. Автоматического сжатия нет. Точное начало между ключевыми кадрами и эффекты могут требовать более долгого кодирования; время также зависит от сети и источника.
- Удаление подходит для простых неподвижных прямоугольников без поворота в 8-битном SDR. На сложном фоне возможны следы.
- Тест прокси проверяет связь. YouTube может отклонить метаданные с `bot_check`; режим «Напрямую» можно выбрать вручную.
- Установщики не подписаны Windows Authenticode. Сверяйте SHA-256 и официальный источник. Не отключайте защиту. Обновления приложения отдельно проверяются подписью Ed25519.

<details>
<summary>English (US)</summary>

A free Windows Chrome extension for downloads and editing directly on YouTube. Every feature is free; media processing stays on your PC.

**New:** faster temporal-clip validation, removal of unnecessary encoding at safe keyframe starts, corrected edited-Shorts/video-clip folders, and clearer copy/encode/validate stages. Ordered packet and timestamp checks preserve the selected original frames, resolution and audio.

Choose the recommended EXE, the standalone ZIP with its included Windows component installer and separate `extension` folder, or the optional Beta/Experimental automatic installer. Standard enrollment is manual in `chrome://extensions`. Use the [English guide](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.71/docs/install/en.md).

Original-quality files can be large. Explicitly select an available 1080p/720p source for a smaller file. There is no automatic compression. Non-keyframe cuts and effects can require slower encoding. Eraser supports stationary unrotated 8-bit SDR rectangles and can leave artifacts. Proxy connectivity does not guarantee YouTube metadata access. Installers are Authenticode unsigned; verify checksums. Ed25519 protects app updates separately. Only YouTube is supported today; more platforms are planned.

</details>

<details>
<summary>Français</summary>

Extension Chrome gratuite pour télécharger et éditer directement sur YouTube, avec traitement local sous Windows. Toutes les fonctions sont gratuites.

Cette version évite le réencodage inutile des extraits commençant sur une image clé, accélère la validation et corrige les dossiers des Shorts édités et des extraits vidéo. Les images, leur chronologie et le son d’origine sont vérifiés.

Choisissez l’EXE recommandé, le ZIP avec son installateur de composants et son dossier `extension` séparé, ou le mode Beta/Experimental non garanti. [Guide français](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.71/docs/install/fr.md). La qualité d’origine peut produire de gros fichiers; sélectionnez explicitement une source 1080p/720p disponible si nécessaire. L’effacement est limité aux rectangles fixes sans rotation en SDR 8 bits. Un proxy accessible peut être refusé par YouTube. Les EXE ne sont pas signés par Authenticode. Seul YouTube est pris en charge actuellement.

</details>

<details>
<summary>Deutsch</summary>

Kostenlose Chrome-Erweiterung für Downloads und Bearbeitung direkt auf YouTube. Die Medienverarbeitung bleibt auf dem Windows-PC; alle Funktionen sind kostenlos.

Diese Version vermeidet unnötiges Kodieren bei geeigneten Schlüsselbild-Anfängen, beschleunigt die Prüfung und korrigiert die Zielordner bearbeiteter Shorts und Videoausschnitte. Originalbilder, Zeitstempel und Audio werden geprüft.

Wählen Sie das empfohlene EXE, das ZIP mit separatem Komponenteninstaller und `extension`-Ordner oder Beta/Experimental ohne Erfolgsgarantie. [Deutsche Anleitung](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.71/docs/install/de.md). Originalqualität kann große Dateien erzeugen; eine verfügbare 1080p/720p-Quelle ist ausdrücklich wählbar. Entfernen unterstützt feste ungedrehte Rechtecke in 8-Bit-SDR. YouTube kann trotz erfolgreichem Proxy-Test Metadaten verweigern. Die EXE-Dateien haben keine Authenticode-Signatur. Derzeit wird nur YouTube unterstützt.

</details>

<details>
<summary>العربية</summary>

<div dir="rtl" lang="ar">

إضافة Chrome مجانية لتنزيل وتحرير فيديوهات YouTube مباشرة، مع معالجة محلية على جهاز Windows. جميع الوظائف مجانية.

يتجنب هذا الإصدار إعادة الترميز غير الضرورية للمقاطع التي تبدأ بإطار مفتاح مناسب، ويسرّع التحقق ويصحح مجلدات Shorts المعدّلة والمقاطع العادية، مع التحقق من الإطارات والتوقيت والصوت الأصلي.

اختر EXE الموصى به، أو ZIP الذي يحتوي مثبّت المكوّنات ومجلد `extension` المنفصل، أو Beta/Experimental غير المضمون. [الدليل العربي](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.71/docs/install/ar.md). قد تكون ملفات الجودة الأصلية كبيرة؛ يمكن اختيار مصدر متاح بدقة 1080p أو 720p صراحةً. تقتصر الإزالة على مستطيلات ثابتة غير مدوّرة في SDR بعمق 8 بت. قد يرفض YouTube الوكيل رغم نجاح الاتصال. المثبّتات غير موقعة بـ Authenticode. يدعم التطبيق YouTube فقط حاليًا.

</div>

</details>

[SHA256SUMS.txt](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/SHA256SUMS.txt) · [Documentation and licenses](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.71/VidoZavr-Documentation.zip)
