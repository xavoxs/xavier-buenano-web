# xavier-buenano-web

Página de perfil profesional de Xavier Buenaño: marketing digital, automatización con IA y desarrollo web.

## Contenido

- `index.html`: la página completa (HTML, CSS y JavaScript en un solo archivo, sin dependencias de instalación).
- `guia-de-estilo.md`: cromática, tipografía, rejilla y componentes.

## Cómo verla

Abre `index.html` en el navegador. Las fuentes se cargan desde Google Fonts, por lo que requiere conexión a internet.

## Pendientes de contenido

- Reemplazar el testimonio de ejemplo (nombre ficticio) por uno real, con permiso para publicar nombre, cargo y empresa.
- Agregar una cifra real por caso cuando se tenga.
- Confirmar con Sotomayor Consulting el permiso para publicar el caso de medición.
- Definir la duración del diagnóstico gratuito (el costo ya está definido: gratuito).
- Correo propio cuando exista el dominio.
- Confirmar el enlace de LinkedIn.

## Estado

Borrador. El repositorio es privado hasta que el contenido esté completo.

## Indexación en Google

Por ahora la página está marcada como `noindex, nofollow` (etiqueta `robots` en `index.html`) para que Google no la muestre mientras se completa el contenido.

Para publicarla en buscadores:
1. En `index.html`, cambiar `noindex, nofollow` por `index, follow, max-image-preview:large`.
2. En `robots.txt`, agregar la línea `Sitemap: https://xavoxs.github.io/xavier-buenano-web/sitemap.xml`.
3. Registrar la propiedad en Google Search Console, enviar el sitemap y solicitar la indexación.
