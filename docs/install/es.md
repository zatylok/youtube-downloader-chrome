# Instalar VidoZavr 1.2.60

**[Русский](ru.md) · [English](en.md) · [Deutsch](de.md) · [Español](es.md) · [Português do Brasil](pt-BR.md)**

Todas las funciones son gratuitas: vídeos de YouTube, Shorts, canales, listas,
emisiones en directo, recorte y gestión de descargas. El procesamiento es local.
Necesita **Windows 11 x64, Chrome 127+ e Internet para la primera instalación**.
No necesita Python, Rust ni Node.js. El componente de Windows conecta Chrome con
las herramientas locales mediante Native Messaging. **La extensión sola no basta.**

## Instalación recomendada: nueve pasos

1. **Descargue [VidoZavr.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr.exe).**
   No necesita descargar también el ZIP. Use la versión oficial y compare
   su [SHA-256](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/SHA256SUMS.txt).
2. **Ejecute el EXE e instale los componentes de Windows.** Setup está en ruso:
   **Далее = Siguiente**, **Готово = Finalizar**. Espere a **Компоненты Windows
   установлены** (componentes de Windows instalados). Se descargan y verifican las
   herramientas fijadas que falten; se reutilizan los archivos válidos ya instalados.
   Setup no abre Chrome ni comprueba una conexión activa con el navegador.
3. **Lea la última pantalla antes de cerrarla.** El campo de ruta muestra la carpeta
   permanente de la extensión. **Папка расширения = Carpeta de la extensión** la abre;
   **Инструкция = Instrucciones** abre la guía instalada. Guarde la ruta exacta para el paso 7.
4. **Abra `chrome://extensions`** en el perfil de Chrome que usa para YouTube.
   Escriba la dirección en la barra: es una página interna, no un sitio web.
5. Active **Modo Desarrollador** en la parte superior derecha.
6. Pulse **Cargar descomprimida**. Se abrirá el selector de carpetas de Windows.
7. **Seleccione exactamente la carpeta instalada `extension` del paso 3.**
   Navegue hasta ella o pegue la ruta exacta de Setup en el campo **Carpeta** y
   confirme con **Seleccionar carpeta** (Windows en ruso: **Папка**, **Выбор папки**).
   `manifest.json` debe estar directamente dentro. Seleccione la carpeta, no el
   archivo, Descargas, la carpeta superior de instalación ni un ZIP.
8. **Compruebe una sola tarjeta V1D0Z@VR 🦖 activada**, versión **1.2.60**.
   En modo de desarrollador, el ID es `bkihgeeibbodemeibfdcglojjkiepnlf`.
9. **Abra el menú Extensiones de Chrome, con el icono de pieza de puzle → V1D0Z@VR.**
   Busque **Downloader connected** si la extensión está en inglés, o **Загрузчик подключён**
   si está en ruso: significa «descargador conectado». Puede fijar su icono.
   La tarjeta por sí sola no confirma la conexión Native.

Carpeta predeterminada:

`%LOCALAPPDATA%\Programs\YouTube Video & Shorts Downloader\extension`

**Una instalación personalizada puede usar otra ruta. La ruta exacta de la última
pantalla de Setup es la referencia.** Conserve esa carpeta permanente y mantenga
activo el modo de desarrollador. Si ya cerró Setup, encontrará las instrucciones en
el menú Inicio; use la carpeta elegida durante la instalación y su subcarpeta `extension`.

### Identificar los controles

La captura está en **inglés**: **1 Developer mode = Modo Desarrollador**,
**2 Load unpacked = Cargar descomprimida**. Chromium 149 real, sin ventana visible;
la captura excluye el espacio sin usar.

![Controles en inglés con los números 1 y 2](images/chrome-controls-en.png)

La tarjeta real muestra nombre, versión, ID e interruptor activado.

![Tarjeta de VidoZavr en Chromium en inglés](images/extension-card-en.png)

<details>
<summary>Ejemplo de conexión confirmada (interfaz rusa)</summary>

**1** señala «Загрузчик подключён», equivalente a «descargador conectado». Esta imagen
existente muestra una respuesta Native real y aislada, no una nueva instalación manual.

![Conexión Native verificada en el menú real](images/connected.png)

</details>

Las imágenes son de perfiles aislados de **Chromium 149 sin ventana visible**,
no de Chrome 156 ni de Windows recién instalado. La tarjeta es una ilustración;
se conserva la [vista completa original](images/chrome-extensions.png).
No se simulan imágenes del final de Setup ni del selector de carpetas.

## Otras opciones

- **Avanzada — [VidoZavr-Extension.zip](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr-Extension.zip):**
  instale el componente Windows con el EXE recomendado, extraiga el ZIP en una carpeta
  permanente independiente y cargue esa carpeta **en lugar de** la copia administrada.
  Chrome no carga un ZIP directamente. Setup y las actualizaciones firmadas no mantienen
  esa copia: sustituya sus archivos con el ZIP oficial correspondiente y recargue su
  tarjeta existente. No cargue ambas copias.
- **Beta/Experimental — [VidoZavr-Experimental.exe](https://github.com/zatylok/youtube-downloader-chrome/releases/download/v1.2.60/VidoZavr-Experimental.exe):**
  intenta conectar Chrome automáticamente usando la misma instalación Windows.
  Puede requerir modo de desarrollador, selección de perfil o decisiones sobre permisos;
  otras extensiones pueden interrumpirlo. No se garantiza el éxito ni una instalación
  totalmente desatendida. La verificación en Windows limpio es incompleta.
  Consulte las [limitaciones](EXPERIMENTAL.md).

## Seguridad y herramientas descargadas

Los EXE **no tienen firma Windows Authenticode**. SmartScreen puede mostrar un editor
desconocido. Verifique la fuente oficial y el hash; cancele si tiene dudas.
Nunca desactive las protecciones. Comprobación opcional: `Get-FileHash .\VidoZavr.exe -Algorithm SHA256`.

Setup obtiene yt-dlp **2026.10.21**, Deno **2.9.8** y FFmpeg/FFprobe **9.0.2**, compilación
Windows de Gyan Doshi, directamente de los proveedores fijados, con comprobación de
tamaño/SHA-256. Esos EXE de terceros no están incluidos en nuestras descargas.
La primera instalación no es completamente sin conexión.
[Componentes, fuentes, licencias y hashes](COMPONENTS.md).
**La firma Ed25519 de las actualizaciones es distinta de la firma del instalador Windows.**

## Actualizar y desinstalar

Las actualizaciones firmadas mantienen la carpeta instalada y esperan mientras haya
trabajo de medios protegido. Si Chrome sigue mostrando una versión antigua después,
pulse **Volver a cargar** en la tarjeta existente de `chrome://extensions` y actualice
las pestañas de YouTube. Conserve la tarjeta y sus preferencias; no se garantiza
activación automática en todas las versiones. Las carpetas ZIP independientes se
actualizan manualmente.

Para reparar, ejecute Setup cuando termine el trabajo y siga cualquier aviso de
archivos ocupados. Conserve tareas pausadas y archivos parciales.
Desinstale en **Configuración de Windows → Aplicaciones → V1D0Z@VR → Desinstalar**;
después elimine la tarjeta de Chrome. Los vídeos, `native\data` y `.updates` permanecen.
Eliminar la tarjeta puede borrar sus ajustes guardados en el navegador.

## Solución de problemas

| Problema | Acción admitida |
|---|---|
| Falta el manifiesto / no se puede cargar | Repita Cargar descomprimida y seleccione exactamente `extension` con `manifest.json` dentro. Descargas, la carpeta superior y el ZIP no sirven. |
| Hay tarjeta, pero el descargador no está conectado | Compruebe el componente Windows para **el mismo usuario de Windows**, el perfil de Chrome y la carpeta exacta. `Check.cmd` en la instalación comprueba archivos/registro; el menú comprueba la conexión activa. Repare con Setup tras terminar el trabajo si hace falta. |
| Modo Desarrollador desactivado | Actívelo en el perfil correcto, manténgalo activo y compruebe que la tarjeta existente está activada. |
| Perfil equivocado o copias duplicadas | Busque el perfil y la carpeta permanente que eligió. No añada otra copia para reparar la conexión; eliminar una tarjeta puede borrar sus ajustes. |
| Actualización terminada, versión antigua en Chrome | Tras finalizar el trabajo protegido, recargue la **tarjeta existente** y las pestañas de YouTube. No borre datos pausados. |
| Red, rutas VPN o fallo de descarga/hash | Compruebe la conexión del descargador, además de Chrome. El túnel dividido puede usar rutas distintas. Reintente la fuente oficial; no use espejos alternativos, cambie hashes ni desactive protecciones. |
| Aviso SmartScreen | El instalador no está firmado. Verifique fuente y suma; cancele si tiene dudas. |
| Experimental bloqueado por otra extensión | No acepte solicitudes ajenas a ciegas ni desactive otras extensiones. Cierre su Setup normalmente y use la instalación manual recomendada. |

Ayuda: [GitHub Issues](https://github.com/zatylok/youtube-downloader-chrome/issues) o
[@zatylok007](https://t.me/zatylok007). Indique versión, error exacto y pasos breves;
nunca envíe cookies, tokens ni perfiles privados.
[Permisos y privacidad](../../README.md#windows-warnings-permissions-and-privacy) ·
[Opciones e idiomas](README.md)
