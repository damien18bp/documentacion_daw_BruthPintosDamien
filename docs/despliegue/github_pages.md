---
sidebar_position: 1
---

# Despliegue en GitHub Pages

## Objetivo

La documentación de GameShelf se publica como un sitio web estático generado con Docusaurus y desplegado automáticamente mediante GitHub Pages.

## Tecnologías utilizadas

- Docusaurus.
- Node.js.
- npm.
- Git.
- GitHub.
- GitHub Actions.
- GitHub Pages.

## Proceso de despliegue

1. Se crea el proyecto de documentación con Docusaurus.
2. Se añaden los documentos Markdown y MDX dentro de la carpeta `docs`.
3. Se configura `docusaurus.config.ts` con la URL de GitHub Pages.
4. Se ejecuta el comando `npm run build`.
5. Docusaurus genera la carpeta `build`.
6. El proyecto se sube a un repositorio de GitHub.
7. GitHub Actions ejecuta el workflow de despliegue.
8. GitHub Pages publica automáticamente el contenido generado.

## Configuración de Docusaurus

La configuración debe incluir una URL y una ruta base correctas:

```ts
url: '[https://TU_USUARIO.github.io](https://TU_USUARIO.github.io)',
baseUrl: '/NOMBRE_DEL_REPOSITORIO/',
```

Por ejemplo, si el repositorio se llama `documentacion-daw`, la ruta base será:

```ts
baseUrl: '/documentacion-daw/',
```

## Workflow de GitHub Actions

El workflow realiza estas tareas:

- Descarga el repositorio.
- Instala las dependencias con `npm ci`.
- Ejecuta `npm run build`.
- Sube la carpeta `build` como artefacto.
- Publica el sitio en GitHub Pages.

Cada vez que se hace un `push` a la rama `main`, GitHub vuelve a generar y publicar la documentación automáticamente.