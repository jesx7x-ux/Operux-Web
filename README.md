# Operux — Landing Page

## Setup rápido (Vercel)
1. Descargar y extraer el ZIP.
2. En Vercel: Crear proyecto → Import folder → Deploy.
   (También sirve para cualquier hosting estático — Hostinger, Netlify, etc. Solo arrastra la carpeta.)

## Cambios necesarios ANTES de ir a producción
- [ ] Reemplazar el número de WhatsApp en `index.html` (buscar `5812345678` dentro del `<script>`, variable `phone`).
- [ ] Cambiar el ID de Formspree (buscar `formspree.io/f/REPLACE_ID` en el `<form>`).
- [ ] Agregar Google Analytics 4 si lo deseas (no está incluido por defecto; pégalo antes de `</body>`).
- [ ] Agregar los links reales de redes sociales en el footer (o quitarlos si no existen).
- [ ] Cambiar la URL canonical en `<head>` al dominio real.
- [ ] Probar el formulario de email en producción.

## Estructura
- `index.html` — todo el contenido con CSS y JS embebidos, un solo archivo.
- `assets/img/` — logo en dos variantes:
  - `logo-black.png/webp` — para fondos claros (header, hero).
  - `logo-white.png/webp` — para fondos oscuros (footer).
- `sitemap.xml`, `robots.txt`, `vercel.json` — SEO y despliegue.

## Rendimiento
- Objetivo Lighthouse: >85 en Performance/Accessibility/SEO.
- Sin dependencias externas salvo Google Fonts (Space Grotesk + Inter).

## Soporte
Si algo no funciona:
1. Abre la consola del navegador (F12 → Console).
2. Verifica que el número de WhatsApp tenga el formato correcto: código de país + número, sin "+".
3. Verifica que el Formspree ID sea válido si usas el formulario de email.
