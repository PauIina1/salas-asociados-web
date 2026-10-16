# Arquitectura del proyecto

## Objetivo

El proyecto usa una arquitectura frontend estática y basada en componentes para un sitio institucional pequeño. Astro genera HTML estático durante la compilación; no existe servidor de aplicación, base de datos ni API propia.

## Organización

- `src/components/layout`: componentes compartidos de estructura, como la cabecera y el pie.
- `src/data`: contenido institucional estructurado en JSON. En esta etapa solo contiene datos provisionales del sitio.
- `src/layouts`: documentos HTML compartidos, metadatos y carga de estilos globales.
- `src/pages`: rutas públicas y composición de cada página.
- `src/styles`: estilos globales e importación de Tailwind CSS.
- `public`: archivos estáticos servidos sin transformación.
- `docs`: documentación técnica del proyecto.

Las carpetas para secciones, componentes visuales genéricos e imágenes se añadirán cuando una iteración las necesite. Así se evita mantener estructuras vacías o abstracciones prematuras.

## Flujo de renderizado

1. `src/pages/index.astro` representa la ruta `/`.
2. La página obtiene el contenido provisional desde `src/data/site.json`.
3. `BaseLayout.astro` aporta la estructura HTML, los metadatos y los estilos globales.
4. Los componentes de `components/layout` aportan la cabecera y el pie reutilizables.
5. Astro genera el resultado estático en `dist/` mediante `npm run build`.

## Decisiones técnicas

- TypeScript extiende `astro/tsconfigs/strict` para detectar errores durante el desarrollo.
- Tailwind CSS 4 se integra mediante `@tailwindcss/vite`, el procedimiento oficial para versiones actuales de Astro.
- No se incorpora un framework de interfaz adicional porque Astro y HTML son suficientes para el alcance actual.
- No se usa JavaScript del lado del cliente en esta etapa.
- El contenido se mantiene separado de la presentación para facilitar su reemplazo cuando se validen los datos reales.

## Accesibilidad y rendimiento

La base define el idioma español, incluye un enlace para saltar al contenido principal, usa regiones semánticas y mantiene foco visible en elementos interactivos. Al no hidratar componentes ni cargar JavaScript del cliente, la página inicial conserva un coste de ejecución reducido.
