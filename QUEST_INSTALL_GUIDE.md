# Guía de Instalación para Meta Quest (Offline)

He optimizado **TODO el proyecto** para que funcione sin internet ("Offline"). Aquí te explico cómo instalarlo y visualizarlo en las gafas Meta Quest.

## Opción A: Copiar y Abrir (Básico)
Esta opción funciona para **todo el sitio web** (Menú Principal, Fairmont, Conecta, etc.).

1.  Conecta las Meta Quest a tu computadora via USB.
2.  Copia la carpeta completa del proyecto `AntigravityWEB` al almacenamiento interno de las Quest (ej. en la carpeta `Download` o `Documents`).
3.  En las Quest, usa una aplicación de explorador de archivos para abrir `hoteles/fairmont.html` con el navegador (Meta Browser o Wolvic).
    *   *Nota: Si el video 360 no carga, usa la Opción B.*

## Opción B: Servidor Local (Recomendado para VR Completo)
Los navegadores modernos bloquean a veces los videos 360 cuando se abren directamente desde un archivo (`file://`) por seguridad. Para evitar esto, se recomienda simular un pequeño servidor.

1.  Instala una aplicación de servidor web simple en las Quest (hay muchas APKs gratuitas para Android, como "Simple HTTP Server").
2.  Copia la carpeta del proyecto a las Quest.
3.  Abre la app de servidor y apunta a la carpeta del proyecto.
4.  Te dará una dirección local (ej. `http://127.0.0.1:8080/hoteles/fairmont.html`).
5.  Abre esa dirección en el navegador de las Quest.

## Resumen de Cambios Realizados
*   **Proyecto Completo Offline:** Se optimizaron `mainmenu.html`, `fairmont.html` y `vr/fairmont-360.html` para no depender de internet.
*   **Librerías Locales:** Swiper, A-Frame y fuentes ahora se cargan desde la carpeta `assets/libs`.
*   **Mapa Híbrido (Inteligente):**
    *   **Sin Internet (Offline):** Muestra una imagen estática elegante con la ubicación.
    *   **Con Internet (Online):** Si se detecta conexión, carga automáticamente el mapa interactivo de Google.
*   **Descargas:** El botón de descargar Reel tiene un sistema de respaldo. Si no puede descargar el archivo como blob (por restricciones de seguridad), intentará abrirlo directamente.
