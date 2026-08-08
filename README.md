# Geoenergía — sitio Astro

Sitio bilingüe (ES/EN) del capítulo estudiantil Geoenergía (Uninorte), construido en Astro. Contenido estático, sin backend.

## Estructura
- `src/data/content.js` — todo el contenido (textos, junta, actividades, noticias) en español e inglés. Editar aquí para actualizar el sitio.
- `src/layouts/Layout.astro` — header, nav, selector de idioma, banner de contacto y footer (compartidos en todas las páginas).
- `src/components/` — tarjetas reutilizables (actividad, fila de junta, noticia).
- `src/pages/` — páginas en español (raíz `/`) y `src/pages/en/` — mismas páginas en inglés.
- `src/pages/actividades/[sem].astro` — página de actividades por semestre (rutas generadas automáticamente: `/actividades/2026-1`, `/actividades/2025-2`, `/actividades/2025-1`, y sus equivalentes en `/en/actividades/...`).
- `public/` — logos.

## Desarrollo local
```
npm install
npm run dev
```

## Despliegue en Vercel
1. Sube este contenido al repositorio de GitHub conectado (`loresofi/Geoenergia`, rama `main`).
2. En [vercel.com](https://vercel.com), "Add New Project" → importa el repo. Vercel detecta Astro automáticamente (build command `astro build`, output `dist`).
3. Deploy. El sitio queda en un subdominio `*.vercel.app` (puedes conectar un dominio propio después desde la configuración del proyecto en Vercel).

## Pendiente / notas
- Los espacios de imagen (posts de noticias, actividades, mascota Peri) están como placeholders grises — reemplázalos por las imágenes reales en cada componente/página cuando estén disponibles.
- El contenido bilingüe vive en un solo archivo (`content.js`) para facilitar mantenerlo sincronizado entre ES y EN.
