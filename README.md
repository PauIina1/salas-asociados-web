# Sitio web de Salas & Asociados

Base técnica del sitio institucional informativo del Estudio Jurídico Salas & Asociados, ubicado en Pampas, Tayacaja, Huancavelica, Perú.

Esta primera etapa contiene únicamente la configuración, la arquitectura mínima y una página de inicio provisional. No incluye backend, base de datos ni funcionalidades de gestión.

## Requisitos

- Node.js 22.22 o superior dentro de la versión 22 LTS.
- npm 10 o superior.

## Instalación

```sh
npm install
```

## Desarrollo local

```sh
npm run dev
```

Astro mostrará en la terminal la dirección local, normalmente `http://localhost:4321`.

## Verificación de tipos

```sh
npm run check
```

## Compilación de producción

```sh
npm run build
```

Los archivos estáticos se generan en `dist/`.

## Vista previa de la compilación

Después de compilar:

```sh
npm run preview
```

## Estructura actual

```text
public/
├── favicon.ico
└── favicon.svg
src/
├── components/
│   └── layout/
│       ├── SiteFooter.astro
│       └── SiteHeader.astro
├── data/
│   └── site.json
├── layouts/
│   └── BaseLayout.astro
├── pages/
│   └── index.astro
└── styles/
    └── global.css
docs/
└── architecture.md
```

Las carpetas `components/sections`, `components/ui` y `public/images` se crearán cuando existan elementos reales que las necesiten.

## Tecnologías

- Astro con generación estática.
- TypeScript en modo estricto.
- Tailwind CSS 4 mediante el plugin oficial para Vite.
- HTML5 semántico.

## Contenido

Los textos visibles de esta etapa son provisionales. Los datos reales del estudio deben validarse antes de publicarse.

## Control de versiones

El proyecto sigue Conventional Commits. Las operaciones de Git y GitHub deben ejecutarse manualmente por la persona responsable del repositorio.
