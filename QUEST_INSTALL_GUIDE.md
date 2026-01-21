# Guía de Instalación para Meta Quest (Offline)

He optimizado **TODO el proyecto** para que funcione sin internet ("Offline"). Aquí te explico cómo instalarlo y visualizarlo en las gafas Meta Quest.

## Opción A: Copiar y Abrir (Básico)
Esta opción funciona para **todo el sitio web** (Menú Principal, Fairmont, Hard Rock, etc.).

1.  Conecta las Meta Quest a tu computadora via USB.
2.  Copia la carpeta completa del proyecto `AntigravityWEB` al almacenamiento interno de las Quest (ej. en la carpeta `Download` o `Documents`).
3.  En las Quest, usa una aplicación de explorador de archivos para abrir `mainmenu.html` o directamente `hoteles/fairmont.html` con el navegador (Meta Browser o Wolvic).
    *   *Nota: Si el video 360 no carga, usa la Opción B.*

## Opción B: Servidor Local (Recomendado para VR Completo)
Los navegadores modernos bloquean a veces los videos 360 cuando se abren directamente desde un archivo (`file://`) por seguridad. Para evitar esto, se recomienda simular un pequeño servidor.

1.  Instala una aplicación de servidor web simple en las Quest (hay muchas APKs gratuitas para Android, como "Simple HTTP Server").
2.  Copia la carpeta del proyecto a las Quest.
3.  Abre la app de servidor y apunta a la carpeta del proyecto.
4.  Te dará una dirección local (ej. `http://127.0.0.1:8080/mainmenu.html`).
5.  Abre esa dirección en el navegador de las Quest.

## Resumen de Cambios Recientes (v2.0)
*   **Propiedades Completas:** Se implementó totalmente **Hard Rock Hotel Cancún** con su propio tour 360 (PRÓXIMAMENTE) y ficha técnica enriquecida.
*   **Proyecto 100% Offline:** Swiper, A-Frame y las fuentes ahora son locales para garantizar que las presentaciones en las gafas no fallen por falta de internet.
*   **Interactividad en Reels:** 
    *   **Click-to-Pause:** Se puede pausar y reanudar el video tocando directamente la pantalla (estilo Instagram).
    *   **Descarga:** Se añadió un sistema de descarga forzada para guardar los videos.
*   **Experiencia Limpia:** Se ocultó el menú de navegación principal en las páginas de detalle para que la demo se enfoque solo en el hotel.
*   **Mapa Híbrido:** Si hay internet, carga Google Maps; si no, muestra una imagen estática de alta calidad.
