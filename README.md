# V1D0Z@VR 🦖

Бесплатный загрузчик для Chrome, который работает прямо на YouTube. Сохраняйте
видео, Shorts, каналы, плейлисты и трансляции, выбирайте качество и управляйте
загрузками в одном месте. Обработка медиа выполняется на вашем Windows-ПК.

A free Chrome extension for YouTube downloads and video tools, with local processing
on Windows. All functions are free, with no PRO tier or subscription.

## [Скачать VidoZavr.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.70/VidoZavr.exe)

Рекомендуемый установщик для Windows 11 x64 и Chrome 127+.
Он устанавливает компоненты Windows и папку расширения. Подключение этой папки
к Chrome выполняется вручную. Дополнительный ZIP не нужен.

## Возможности

- **Видео и Shorts прямо на YouTube.** Скачивание без перехода на сторонний сайт.
- **Высокое качество.** 1080p, 1440p (2K), 4K, 60 FPS и HDR, когда они доступны у
  источника и совместимы с выбранными настройками.
- **Текущие LIVE-трансляции.** Запись с начала эфира, если оно доступно, с продолжением
  до завершения трансляции.
- **Каналы и плейлисты.** Загрузка видео из подборок и со страниц каналов.
- **Единый редактор видео и Shorts.** Выбирайте область кадра и интервал для
  скачивания. Черновики сохраняются отдельно для каждого видео.
- **До восьми масок с независимыми интервалами.** Размытие, пикселизация и
  заливка поддерживают поворот. «Удаление ✨» интерполирует пиксели локально
  через FFmpeg и показывает обработанный стоп-кадр, когда он доступен.
  Удаление подходит для неподвижных прямоугольников без поворота на 8-битном
  SDR. На сложном фоне могут остаться следы.
- **Возобновление загрузок.** Использование сохранённых данных, когда источник
  поддерживает безопасное продолжение.
- **Управление задачами.** До десяти одновременных загрузок, индивидуальный
  прогресс, отмена и настраиваемые папки.
- **Пул прокси и история обновлений.** Десять слотов HTTP/SOCKS5 с защищённым
  хранением учётных данных и история до десяти известных версий.
- **Удобство просмотра.** Автопрокрутка Shorts, тёмная и светлая темы.
- **Качество воспроизведения YouTube.** Автоматический выбор максимального доступного
  качества или ручной выбор другого варианта во время просмотра. Настройка относится
  к просмотру видео; качество скачиваемого файла выбирается отдельно.

Все функции бесплатны. Нет PRO, подписок или платных ограничений.
Качество и доступность начала LIVE зависят от исходного видео и выбранного формата.

Успешный тест прокси подтверждает связь. YouTube может отказать в выдаче
метаданных с кодом `bot_check` и через работающий прокси. При необходимости
выберите режим «Напрямую» вручную.

## Варианты установки

| Вариант | Файл | Как работает |
|---|---|---|
| **Рекомендуется** | **[VidoZavr.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.70/VidoZavr.exe)** | Устанавливает компоненты Windows и управляемую папку расширения. Затем подключите её вручную в Chrome. |
| Автономный ZIP | [VidoZavr-Extension.zip](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.70/VidoZavr-Extension.zip) | Распакуйте архив в постоянную папку и запустите вложенный `Установить компоненты.exe`. Затем вручную загрузите отдельную папку `extension` из ZIP. |
| **Beta/Experimental** | [VidoZavr-Experimental.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.70/VidoZavr-Experimental.exe) | Пробует подключить Chrome автоматически. Возможны выбор профиля, запросы разрешений и блокировки другими расширениями. Успех не гарантируется. |

Все варианты используют один ID расширения и одну регистрацию. Выберите один способ установки.
[Ограничения Experimental](docs/install/EXPERIMENTAL.md) описаны отдельно.

## Инструкции

**[Русский](docs/install/ru.md) | [English (US)](docs/install/en.md) | [Français](docs/install/fr.md) | [Deutsch](docs/install/de.md) | [العربية](docs/install/ar.md)**

Это пять языков интерфейса расширения и полных руководств. Сам установщик Windows
остаётся на русском языке.

После установки откройте `chrome://extensions`, включите режим разработчика и
загрузите папку `extension`, указанную в Setup, или папку `extension` из распакованного ZIP.
Внутри должен находиться `manifest.json`. Откройте V1D0Z@VR через меню расширений
Chrome и проверьте статус **«Загрузчик подключён»**.

Папка по умолчанию:

`%LOCALAPPDATA%\Programs\YouTube Video & Shorts Downloader\extension`

Если выбрано другое место установки, используйте путь из Setup.
Подробные шаги, обновление, удаление и [решение частых проблем](docs/install/ru.md#частые-проблемы)
есть в руководствах.

## Что дальше

🦖 V1D0Z@VR продолжает развиваться! Сейчас поддерживается YouTube, включая Shorts и прямые трансляции. В будущем планируем добавить другие социальные сети и видеоплатформы.

V1D0Z@VR keeps evolving. YouTube, including Shorts and LIVE, is supported today.
We plan to add more social networks and video platforms in the future.

<a id="windows-warnings-permissions-and-privacy"></a>

## Требования и безопасность

Нужны Windows 11 x64, Chrome 127+ и интернет для первой установки.
Windows-компонент связывает браузер с локальными инструментами через Native Messaging.
Отдельно устанавливать Python, Rust или Node.js и вручную настраивать реестр не нужно.

Setup и установщик компонентов получают недостающие yt-dlp, Deno и FFmpeg/FFprobe напрямую у закреплённых
поставщиков, проверяя размер и SHA-256. Их EXE не включены в наши пакеты.
[Компоненты, источники и лицензии](docs/install/COMPONENTS.md) описаны подробно.

Установщики **не подписаны Windows Authenticode**, поэтому возможны предупреждения
SmartScreen. Сверьте [контрольные суммы](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.70/SHA256SUMS.txt)
и официальный источник; при сомнении отмените запуск. Не отключайте защиту.
Обновления приложения проверяются подписью **Ed25519**. Это отдельная защита,
которая не заменяет Windows-подпись установщика.

Медиа обрабатываются локально; для получения видео, компонентов и обновлений нужна сеть.
Разрешения браузера и сетевые обращения описаны в
[подробной документации](docs/install/COMPONENTS.md#later-downloads-and-failures).

Оригинальный код распространяется по [MIT](LICENSE). У сторонних компонентов свои
лицензии. V1D0Z@VR не связан с YouTube или Google.

<details>
<summary>English overview</summary>

V1D0Z@VR downloads YouTube videos and Shorts directly on YouTube, including channel
and playlist videos. Available source quality can include 1080p, 1440p (2K), 4K,
60 FPS and HDR, depending on your settings and output format.

Record ongoing LIVE from the original broadcast beginning when it is available,
and continue to completion. The shared video and Shorts editor supports spatial
cropping, time-range trimming, saved drafts and up to eight independently timed
masks. Blur, pixelation and solid fill support rotation. Eraser uses local FFmpeg
interpolation for stationary, unrotated rectangles in 8-bit SDR. A processed
still is available when the source frame can be read. Complex backgrounds can
show artifacts.

Resume interrupted downloads where the source supports continuation. Manage up
to ten simultaneous downloads with progress, cancellation and configurable
folders. The ten-slot HTTP/SOCKS5 proxy pool protects credentials, and Updates
retains up to ten known versions. A successful proxy test confirms connectivity.
YouTube may still return `bot_check` during metadata retrieval. Choose Direct
manually when appropriate. Automatic Shorts scrolling and light/dark themes
are included.
For YouTube playback, select the highest available quality automatically or choose
another available quality manually while watching. Playback quality controls the
video you watch; download quality has its own setting.
Media processing is local. Every function is free.

The recommended EXE installs Windows components. Load its installed extension folder
manually in Chrome; no extra ZIP is needed. The ZIP contains a separate `extension` folder and `Установить компоненты.exe`.
Run the included EXE to install Windows components, then load the extracted
folder manually. Update both ZIP components manually using the next official archive. The automatic installer is Beta/Experimental,
may require user decisions and is not guaranteed.

Use Windows 11 x64 and Chrome 127+. Setup is Russian; the complete
[English (US) guide](docs/install/en.md) explains its labels.
Installers lack Windows Authenticode signing. Verify the official source and
checksums; do not disable security. Ed25519 authenticates application updates
separately. [Component details and licenses](docs/install/COMPONENTS.md).

</details>
