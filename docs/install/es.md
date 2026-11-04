# Instalar VidoZavr 1.2.60

[Opciones e idiomas](README.md) · [Componentes](COMPONENTS.md)

## Función y requisitos

V1D0Z@VR descarga gratis vídeos de YouTube, Shorts, canales, listas y emisiones
en directo, con recorte y gestión de tareas. El procesamiento se realiza localmente.
El componente de Windows conecta Chrome con yt-dlp, Deno y FFmpeg mediante Native
Messaging; la extensión sola no basta. Se necesita Windows 11 x64, Chrome e Internet
para la primera instalación. No hace falta instalar Python, Rust ni Node.js.

## Descargar y verificar

Use las [versiones oficiales](https://github.com/zatylok/youtube-downloader-chrome/releases).
Elija los archivos 1.2.60 de la misma versión oficial.
Descargue **VidoZavr.exe** y su `.sha256`. El ZIP de la extensión es opcional.
Compare SHA-256 con `SHA256SUMS.txt` de la misma versión, por ejemplo con
`Get-FileHash .\VidoZavr.exe -Algorithm SHA256`. Solo lee el archivo;
la instalación no requiere comandos ni cambios manuales en el Registro.

El EXE **no tiene firma Windows Authenticode**. SmartScreen puede mostrar un editor
desconocido. Verifique origen y hash; cancele si tiene dudas. No desactive las
protecciones. La firma Ed25519 de las actualizaciones es una verificación distinta.

## Instalar Windows

El instalador está en ruso: **Далее significa Siguiente**, **Готово, Finalizar**.
Ejecute el EXE recomendado y espere «Компоненты Windows установлены» (componentes
de Windows instalados). Setup obtiene y verifica las herramientas fijadas que falten;
reutiliza las versiones existentes verificadas. No abre Chrome ni afirma haber
comprobado una conexión activa. La última página muestra la carpeta exacta.
**Инструкция** abre las instrucciones; **Папка расширения**, esa carpeta.
Estas acciones requieren que usted pulse el botón correspondiente.

## Conectar Chrome manualmente

1. En el perfil deseado, abra `chrome://extensions`.
2. Active **Modo de desarrollador**.
3. Pulse **Cargar descomprimida**.
4. Elija la carpeta `extension` indicada por Setup. Ruta predeterminada:
   `%LOCALAPPDATA%\Programs\YouTube Video & Shorts Downloader\extension`.
   Debe contener `manifest.json` directamente.
5. Compruebe una sola tarjeta V1D0Z@VR y el ID `bkihgeeibbodemeibfdcglojjkiepnlf`.
6. Abra el menú: busque **Downloader connected** (descargador conectado) o el estado
   equivalente en el idioma configurado en la extensión.

Mantenga activo el modo de desarrollador. Lea y decida las solicitudes de permisos;
Setup no evita la seguridad del navegador.

## ZIP y Experimental

El EXE ya instala la copia administrada: no extraiga otra innecesariamente.
Para una copia independiente, extraiga el ZIP en una carpeta permanente y selecciónela
en lugar de la instalada. Chrome no carga el ZIP directamente. El componente Windows
sigue siendo obligatorio. No cargue ambas copias. Una carpeta independiente requiere
sustituir los archivos con el ZIP oficial correspondiente y recargar la tarjeta existente.

La variante [Beta/Experimental](EXPERIMENTAL.md) conserva la conexión automática.
Puede requerir el modo de desarrollador, decisiones sobre permisos o recuperación
manual. Otras extensiones o la selección de perfiles pueden bloquearla. No está
garantizada ni es totalmente desatendida; la verificación en Windows limpio es incompleta.
Ambos instaladores usan la misma instalación, no dos aplicaciones.

## Actualizar y desinstalar

Las actualizaciones firmadas mantienen la carpeta instalada y esperan a que termine
el trabajo protegido. Si Chrome muestra una versión antigua, recargue la tarjeta
existente en `chrome://extensions` y las pestañas de YouTube. No se garantiza activación
automática en todas las versiones. No elimine la tarjeta para actualizar.
Ejecute Setup de nuevo para reparar tras finalizar las descargas. Si la protección
informa de archivos ocupados, desactive temporalmente la extensión cuando lo solicite.
Conserve tareas pausadas y archivos parciales. Desinstale desde Configuración de Windows
→ Aplicaciones → V1D0Z@VR; después elimine la tarjeta de Chrome. Los vídeos,
`native\data` y `.updates` se conservan.

## Problemas habituales

- Sin conexión: revise usuario Windows, componente instalado y carpeta exacta;
  repare después de terminar el trabajo y reinicie Chrome.
- Falta el manifiesto: elija la carpeta extraída, no el ZIP ni su carpeta superior.
- Red/hash: repita la fuente oficial, sin cambiar los hashes esperados. Chrome y
  el descargador pueden usar rutas VPN distintas.
- Una instalación nueva sin Internet no obtiene herramientas ausentes. La reparación
  puede reutilizar archivos verificados; no se promete funcionamiento totalmente sin conexión.
- `Check.cmd` verifica archivos y registro; la conexión activa se comprueba en el menú.

## Ilustraciones

Chromium 149 real, aislado y sin ventana visible, con interfaz rusa y números
añadidos: **1** modo de desarrollador, **2** cargar descomprimida. Este perfil vacío
no demuestra una instalación manual ni una prueba en Windows limpio.

![Modo de desarrollador y carga de carpeta](images/chrome-extensions.png)

El menú real de la extensión recibió una respuesta Native válida.
**1** señala el descargador conectado. No se usaron cuentas ni perfiles personales.

![Estado de conexión](images/connected.png)

[README](../../README.md): permisos y red. [Auditoría](COMPONENTS.md): fuentes y licencias.
