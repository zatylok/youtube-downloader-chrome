# V1D0Z@VR 1.2.70 🦖

Бесплатное расширение Chrome для загрузок и редактирования прямо на YouTube.
Обработка выполняется на вашем Windows-ПК. Все функции бесплатны.

## Что изменилось после 1.2.63

- Один редактор для обычных видео и Shorts. Выбирайте время начала и конца, обрезайте область кадра и продолжайте редактирование из автоматически сохранённого черновика.
- До восьми масок с отдельными интервалами. Размытие, пикселизация и заливка поддерживают поворот.
- «Удаление ✨» заполняет область локальной интерполяцией FFmpeg. Обработанный стоп-кадр доступен, когда редактор может прочитать исходный кадр. Для экспорта подходят неподвижные прямоугольники без поворота на 8-битном SDR. HDR и 10-битные потоки для удаления не поддерживаются. Сложный фон может оставить заметные следы.
- Компактные настройки пула из десяти прокси HTTP/SOCKS5 и понятные причины ошибок. Учётные данные защищены Windows DPAPI. Успешный тест подтверждает связь, но YouTube может вернуть `bot_check` при запросе метаданных. При необходимости выберите «Напрямую» вручную.
- Страница обновлений хранит до десяти известных версий и различает установленную и проверенную публичную версии.

По-прежнему доступны до десяти одновременных загрузок, выбор качества скачивания и воспроизведения, каналы, плейлисты, запись LIVE с доступного начала, возобновление при поддержке источником, очередь, прогресс и папки. 4K, 60 FPS и HDR зависят от источника и формата. Другие платформы планируются. Сейчас поддерживается YouTube.

## Установка

1. **Рекомендуется [VidoZavr.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.70/VidoZavr.exe).** Запустите Setup. В `chrome://extensions` включите режим разработчика и загрузите распакованную папку `extension`, указанную в Setup.
2. **[Автономный ZIP](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.70/VidoZavr-Extension.zip).** Распакуйте в постоянную папку. Запустите вложенный `Установить компоненты.exe`, затем отдельно подключите папку `extension` из ZIP. Обновляйте обе части вручную.
3. **[Beta/Experimental](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.70/VidoZavr-Experimental.exe).** Пробует подключить Chrome автоматически. Возможны выбор профиля, режим разработчика, запросы разрешений или блокировка сторонним расширением.

Windows 11 x64, Chrome 127+ и интернет для первой установки. Setup проверяет закреплённые инструменты, полученные напрямую у их поставщиков. Установщики не имеют подписи Windows Authenticode, поэтому возможны предупреждения SmartScreen. Сверьте SHA-256. Управляемые установки проверяют подпись Ed25519 обновлений.

## English (US)

A free Windows Chrome extension for downloading and editing directly on YouTube. All features are free and media processing stays on your PC.

**New since 1.2.63.** One editor for videos and Shorts combines time-range trimming, spatial cropping and automatic per-video drafts. Add up to eight independently timed masks. Blur, pixelation and solid fill support rotation. Eraser uses local FFmpeg interpolation and can show a processed still when a source frame is readable. Eraser export supports stationary, unrotated rectangles in 8-bit SDR. HDR and 10-bit Eraser exports are unsupported. Complex backgrounds can show artifacts.

The compact proxy settings offer ten HTTP/SOCKS5 slots with Windows-protected credentials and clearer diagnostics. A successful test confirms connectivity. YouTube may still refuse metadata with `bot_check`. Select Direct manually when appropriate. Updates retains up to ten known versions and distinguishes the installed version from verified public releases.

Existing features include up to ten simultaneous downloads, separate download and playback quality controls, channels, playlists, LIVE recording from the beginning when available, resumable downloads where supported and a task queue with progress and folders. 4K, 60 FPS and HDR depend on the source and format. YouTube is supported today. More platforms are planned.

**Install.** Use the standard EXE and load the folder shown by Setup in Chrome. For the standalone ZIP, run its included Windows component installer, then load the separate extracted `extension` folder. Update both ZIP parts manually. Experimental attempts automatic Chrome enrollment and can require user action. Windows installers are Authenticode unsigned. Verify their checksums. Ed25519 protects managed application updates separately.

## Français

L’éditeur commun aux vidéos YouTube et aux Shorts réunit le découpage temporel, le recadrage, les brouillons automatiques et huit masques au maximum. Le flou, la pixellisation et l’aplat sont orientables. L’effacement et son aperçu fixe utilisent FFmpeg localement. L’export est limité aux rectangles fixes sans rotation en SDR 8 bits. Un fond complexe peut laisser des traces. Le pool compte dix emplacements HTTP/SOCKS5 et le journal conserve dix versions au maximum. YouTube peut refuser les métadonnées (`bot_check`) après un test de connexion réussi. Vous pouvez choisir le mode direct manuellement.

Toutes les fonctions sont gratuites. Pour l’EXE standard, chargez le dossier indiqué par Setup dans Chrome. Pour le ZIP, installez d’abord le composant inclus puis chargez le dossier `extension` séparé. Les deux parties du ZIP se mettent à jour manuellement. Le mode Experimental peut demander une intervention. Les EXE ne sont pas signés par Authenticode.

## Deutsch

Der gemeinsame Editor für YouTube-Videos und Shorts bietet Zeitausschnitte, Zuschneiden, automatische Entwürfe und bis zu acht Masken mit eigenen Zeitintervallen. Unschärfe, Verpixelung und Farbfüllung sind drehbar. Die Entfernung und ihr Vorschaubild nutzen FFmpeg lokal. Der Export unterstützt feste, ungedrehte Rechtecke in 8-Bit-SDR. Komplexe Hintergründe können sichtbare Spuren zeigen. Es gibt zehn HTTP/SOCKS5-Proxyplätze und einen Verlauf für bis zu zehn Versionen. YouTube kann Metadaten trotz erfolgreichem Proxy-Test mit `bot_check` verweigern. Bei Bedarf können Sie manuell den Direktmodus wählen.

Alle Funktionen sind kostenlos. Laden Sie nach dem Standard-Setup den dort gezeigten Ordner in Chrome. Beim ZIP führen Sie zuerst den enthaltenen Komponenteninstaller aus und laden dann den separaten Ordner `extension`. Beide ZIP-Teile werden manuell aktualisiert. Experimental kann Eingaben erfordern. Die EXE-Dateien haben keine Authenticode-Signatur.

## العربية

<div dir="rtl" lang="ar">

يجمع محرّر فيديوهات YouTube وShorts بين اختيار المقطع الزمني وقص الإطار وحفظ المسودات تلقائيًا وإضافة ما يصل إلى ثمانية أقنعة بتوقيت مستقل. يمكن تدوير التمويه والبكسلة والتعبئة اللونية. تستخدم الإزالة ومعاينة الصورة الثابتة FFmpeg محليًا. يقتصر تصدير الإزالة على مستطيلات ثابتة وغير مدوّرة ضمن فيديو SDR بعمق 8 بت. قد تترك الخلفيات المعقّدة آثارًا. تتوفر عشرة مواضع لوكلاء HTTP/SOCKS5 وسجل حتى عشرة إصدارات. قد يرفض YouTube البيانات الوصفية بالرمز `bot_check` رغم نجاح اختبار الوكيل. يمكن اختيار الاتصال المباشر يدويًا.

جميع الوظائف مجانية. بعد تشغيل المثبّت القياسي، حمّل المجلد الذي يعرضه في Chrome. في حزمة ZIP شغّل مثبّت المكوّنات المرفق ثم حمّل مجلد `extension` المنفصل. حدّث الجزأين يدويًا. قد يحتاج التثبيت التجريبي إلى تدخّل المستخدم. ملفات EXE لا تحمل توقيع Authenticode.

</div>

[Русский](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.70/docs/install/ru.md) |
[English (US)](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.70/docs/install/en.md) |
[Français](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.70/docs/install/fr.md) |
[Deutsch](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.70/docs/install/de.md) |
[العربية](https://github.com/zatylok/youtube-downloader-chrome/blob/v1.2.70/docs/install/ar.md)

[SHA256SUMS.txt](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.70/SHA256SUMS.txt) |
[Documentation and licenses](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.70/VidoZavr-Documentation.zip)
