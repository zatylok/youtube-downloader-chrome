# V1D0Z@VR 🦖

Бесплатный загрузчик для Chrome, который работает прямо на YouTube. Сохраняйте
видео, Shorts, каналы, плейлисты и трансляции, выбирайте качество и управляйте
загрузками в одном месте. Обработка медиа выполняется на вашем Windows-ПК.

A free Chrome extension for YouTube downloads and video tools, with local processing
on Windows. All functions are free, with no PRO tier or subscription.

## [Скачать VidoZavr.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.62/VidoZavr.exe)

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
- **Обрезка Shorts.** Выбор области кадра для сохранения.
- **Отрезки видео.** Задайте время начала и конца, чтобы скачать нужную часть ролика.
- **Возобновление загрузок.** Использование сохранённых данных, когда источник
  поддерживает безопасное продолжение.
- **Управление задачами.** Очередь, индивидуальный прогресс, отмена и настраиваемые папки.
- **Удобство просмотра.** Автопрокрутка Shorts, тёмная и светлая темы.
- **Качество воспроизведения YouTube.** Автоматический выбор максимального доступного
  качества или ручной выбор другого варианта во время просмотра. Настройка относится
  к просмотру видео; качество скачиваемого файла выбирается отдельно.

Все функции бесплатны. Нет PRO, подписок или платных ограничений.
Качество и доступность начала LIVE зависят от исходного видео и выбранного формата.

## Варианты установки

| Вариант | Файл | Как работает |
|---|---|---|
| **Рекомендуется** | **[VidoZavr.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.62/VidoZavr.exe)** | Устанавливает компоненты Windows и управляемую папку расширения. Затем подключите её вручную в Chrome. |
| Для опытных пользователей | [VidoZavr-Extension.zip](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.62/VidoZavr-Extension.zip) | Независимая папка расширения с ручным обновлением файлов. Windows Native Host из EXE всё равно обязателен. |
| **Beta/Experimental** | [VidoZavr-Experimental.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.62/VidoZavr-Experimental.exe) | Пробует подключить Chrome автоматически. Возможны выбор профиля, запросы разрешений и блокировки другими расширениями. Успех не гарантируется. |

Оба установщика используют одну установку. Не загружайте две копии расширения.
[Ограничения Experimental](docs/install/EXPERIMENTAL.md) описаны отдельно.

## Инструкции

**[Русский](docs/install/ru.md) | [English (US)](docs/install/en.md) | [Français](docs/install/fr.md) | [Deutsch](docs/install/de.md) | [العربية](docs/install/ar.md)**

Это пять языков интерфейса расширения и полных руководств. Сам установщик Windows
остаётся на русском языке.

После установки откройте `chrome://extensions`, включите режим разработчика и
загрузите точную папку `extension`, указанную на последнем экране Setup.
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

Setup получает недостающие yt-dlp, Deno и FFmpeg/FFprobe напрямую у закреплённых
поставщиков, проверяя размер и SHA-256. Их EXE не включены в наши пакеты.
[Компоненты, источники и лицензии](docs/install/COMPONENTS.md) описаны подробно.

Установщики **не подписаны Windows Authenticode**, поэтому возможны предупреждения
SmartScreen. Сверьте [контрольные суммы](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.62/SHA256SUMS.txt)
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
and continue to completion. Crop the visible area of a Short, resume interrupted
downloads where the source supports continuation, and manage tasks with progress,
cancellation and configurable folders. Automatic Shorts scrolling and light/dark
themes are included. Set a start and end time to download a video segment.
For YouTube playback, select the highest available quality automatically or choose
another available quality manually while watching. Playback quality controls the
video you watch; download quality has its own setting.
Media processing is local. Every function is free.

The recommended EXE installs Windows components. Load its installed extension folder
manually in Chrome; no extra ZIP is needed. The standalone ZIP requires the Windows
Native Host and manual file updates. The automatic installer is Beta/Experimental,
may require user decisions and is not guaranteed.

Use Windows 11 x64 and Chrome 127+. Setup is Russian; the complete
[English (US) guide](docs/install/en.md) explains its labels.
Installers lack Windows Authenticode signing. Verify the official source and
checksums; do not disable security. Ed25519 authenticates application updates
separately. [Component details and licenses](docs/install/COMPONENTS.md).

</details>
