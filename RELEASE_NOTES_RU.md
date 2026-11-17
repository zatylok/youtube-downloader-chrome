**V1D0Z@VR 1.2.72 🦖** - бесплатное расширение Chrome для загрузок и редактирования прямо на YouTube. Все функции бесплатны, обработка медиа выполняется на вашем Windows-ПК.

## Скачать и установить

| Вариант | Для кого |
|---|---|
| **[VidoZavr.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.72/VidoZavr.exe)** | **Рекомендуется.** Устанавливает компоненты Windows и папку расширения. Подключите эту папку к Chrome вручную. Дополнительный ZIP не нужен. |
| [Автономный ZIP](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.72/VidoZavr-Extension.zip) | Распакуйте в постоянную папку. Запустите вложенный `Установить компоненты.exe`, затем отдельно подключите папку `extension`. Обе части обновляются вручную. |
| [Beta/Experimental](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.72/VidoZavr-Experimental.exe) | Пробует подключить Chrome автоматически. Возможны режим разработчика, выбор профиля и запросы разрешений. Успех не гарантируется. |

Для ручного подключения откройте `chrome://extensions`, включите режим разработчика и нажмите «Загрузить распакованное расширение». Выберите именно папку `extension` с `manifest.json`. Нужны Windows 11 x64, Chrome 127+ и интернет при первой установке.

[Русский](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.72/docs/install/ru.md) | [English (US)](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.72/docs/install/en.md) | [Français](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.72/docs/install/fr.md) | [Deutsch](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.72/docs/install/de.md) | [العربية](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.72/docs/install/ar.md)

## Новое в 1.2.72

- **Маски от начала отрезка.** Их время начинается с 00:00 выходного видео. При изменении границ отрезка относительные интервалы сохраняются.
- **Согласованный редактор.** Предпросмотр обрезки по времени, кадру и масок работает вместе; старые черновики сохраняют свой смысл.
- **Автопрокрутка после загрузок.** Исправлен пропуск первого перехода Shorts.
- **История и понятные ошибки.** Добавлены 1.2.71 и 1.2.72 в историю десяти версий, исправлены отметки публичных релизов. Причина отказа при повреждённых временных метках объясняется точнее.

[**Посмотреть интерфейс и примеры редактора**](https://github.com/zatylok/youtube-downloader-chrome/tree/v1.2.72#как-выглядит-vidozavr)

По-прежнему доступны видео, Shorts, каналы, плейлисты, LIVE с доступного начала, восемь масок, поворот, «Удаление ✨», черновики, возобновление, десять одновременных загрузок и прокси. Качество просмотра и скачивания выбирается отдельно. Сейчас поддерживается YouTube; другие платформы планируются.

## Важно

- Исходное качество может давать большие файлы. Для меньшего доступного исходника явно выберите «До 1080p» или «До 720p». Автоматического сжатия нет. Эффекты и точные границы между ключевыми кадрами могут требовать кодирования. Повреждённые потоки по-прежнему отклоняются.
- Удаление подходит для простых неподвижных прямоугольников без поворота в 8-битном SDR. На сложном фоне возможны следы.
- Тест прокси проверяет связь; YouTube может отказать с `bot_check`. Режим «Напрямую» выбирается вручную.
- Установщики не подписаны Windows Authenticode. Сверяйте SHA-256 и официальный источник, не отключайте защиту. Обновления приложения отдельно проверяются Ed25519.

<details>
<summary>English (US)</summary>

Free Windows Chrome extension for downloading and editing directly on YouTube. All features are free; media processing stays on your PC.

**New:** mask times are relative to the output clip, combined trim/crop/mask previews agree, and legacy drafts retain their meaning. Fixed a missed first Shorts transition after downloads. Ten-version history includes 1.2.71/72 with accurate publication labels. Damaged-timestamp errors are clearer; quality checks remain strict.

Choose the recommended EXE, the standalone ZIP with its component installer and separate `extension` folder, or optional Beta/Experimental. Standard Chrome enrollment is manual in `chrome://extensions`. [English guide](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.72/docs/install/en.md).

Original-quality files may be large. Explicitly choose an available 1080p/720p source if wanted; there is no automatic compression. Effects and non-keyframe cuts may encode more slowly. Eraser supports stationary unrotated 8-bit SDR rectangles and may leave artifacts. Proxy connectivity does not guarantee YouTube access. Installers are Authenticode unsigned; verify checksums. Ed25519 protects app updates separately. Only YouTube is supported today.

</details>

<details>
<summary>Français</summary>

Extension Chrome gratuite pour télécharger et éditer directement sur YouTube. Toutes les fonctions sont gratuites; les médias sont traités sur votre PC Windows.

Les temps des masques sont relatifs à l’extrait exporté. Les aperçus du découpage, du recadrage et des masques concordent, et les anciens brouillons conservent leur sens. Le premier passage au Short suivant après un téléchargement est corrigé. L’historique affiche dix versions avec leurs statuts; les erreurs d’horodatage sont plus claires sans affaiblir la qualité.

Choisissez l’EXE recommandé, le ZIP avec son installateur de composants et son dossier `extension`, ou Beta/Experimental sans garantie. [Guide français](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.72/docs/install/fr.md). La qualité d’origine peut produire de gros fichiers; une source 1080p/720p disponible reste un choix explicite. L’effacement est limité aux rectangles fixes sans rotation en SDR 8 bits et peut laisser des traces. Un proxy accessible peut être refusé par YouTube. Les EXE ne sont pas signés par Authenticode; vérifiez les sommes de contrôle. Seul YouTube est pris en charge.

</details>

<details>
<summary>Deutsch</summary>

Kostenlose Chrome-Erweiterung für Downloads und Bearbeitung direkt auf YouTube. Alle Funktionen sind kostenlos; die Medienverarbeitung bleibt auf dem Windows-PC.

Maskenzeiten beziehen sich auf den ausgegebenen Ausschnitt. Vorschauen von Zeitbeschnitt, Bildausschnitt und Masken stimmen überein; alte Entwürfe behalten ihre Bedeutung. Der erste Shorts-Wechsel nach Downloads ist korrigiert. Der Verlauf zeigt zehn Versionen mit ihren Veröffentlichungsständen; Zeitstempelfehler werden klarer erklärt, der Qualitätsschutz bleibt streng.

Wählen Sie das empfohlene EXE, das ZIP mit Komponenteninstaller und separatem `extension`-Ordner oder Beta/Experimental ohne Erfolgsgarantie. [Deutsche Anleitung](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.72/docs/install/de.md). Originalqualität kann große Dateien erzeugen; eine verfügbare 1080p/720p-Quelle muss ausdrücklich gewählt werden. Entfernen unterstützt feste ungedrehte Rechtecke in 8-Bit-SDR und kann Spuren hinterlassen. YouTube kann einen erreichbaren Proxy ablehnen. Die EXE-Dateien sind nicht mit Authenticode signiert; prüfen Sie die Hashwerte. Nur YouTube wird unterstützt.

</details>

<details>
<summary>العربية</summary>

<div dir="rtl" lang="ar">

إضافة Chrome مجانية للتنزيل والتحرير مباشرة على YouTube. جميع الوظائف مجانية، وتبقى معالجة الوسائط على جهاز Windows الخاص بك.

تُحسب أوقات الأقنعة من بداية المقطع الناتج. تتوافق معاينات القص الزمني واقتصاص الإطار والأقنعة، وتحتفظ المسودات القديمة بمعناها. أُصلح أول انتقال بين Shorts بعد التنزيل. يعرض السجل عشرة إصدارات وحالات نشرها، مع توضيح أخطاء الطوابع الزمنية والحفاظ على حماية الجودة.

اختر EXE الموصى به، أو ZIP الذي يحتوي مثبّت المكوّنات ومجلد `extension` المنفصل، أو Beta/Experimental غير المضمون. [الدليل العربي](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.72/docs/install/ar.md). قد تكون ملفات الجودة الأصلية كبيرة؛ يُختار مصدر متاح بدقة 1080p أو 720p صراحةً. تدعم الإزالة مستطيلات ثابتة غير مدوّرة في SDR بعمق 8 بت وقد تترك آثارًا. قد يرفض YouTube الوكيل رغم نجاح الاتصال. المثبّتات غير موقعة بـ Authenticode؛ تحقّق من قيم التجزئة. يدعم التطبيق YouTube فقط حاليًا.

</div>

</details>

[SHA256SUMS.txt](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.72/SHA256SUMS.txt) · [Documentation and licenses](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.72/VidoZavr-Documentation.zip)
