# 🧩 Portafolio Personal – Migración a Astro + TailwindCSS

## 🚀 Descripción del Proyecto

Este proyecto corresponde a mi **portafolio web personal**, el cual inició a partir de una plantilla base proporcionada por el profesor.  
En un inicio se trabajó con **HTML, CSS y Bootstrap**, pero luego se solicitó **migrar el proyecto a Astro y TailwindCSS**, manteniendo la estructura y el contenido original, pero modernizando el código y la organización.

---

## 🧱 Estructura del Proyecto (versión Astro)

📁 src/
┣ 📁 components/
┣ 📁 layouts/
┃ ┗ 📄 Base.astro
┣ 📁 pages/
┃ ┣ 📄 index.astro
┃ ┣ 📄 sobremi.astro
┃ ┣ 📄 proyectos.astro
┃ ┣ 📄 habilidades.astro
┃ ┗ 📄 contacto.astro
┣ 📁 styles/
┃ ┣ 📄 global.css
┃ ┣ 📄 index.css
┃ ┣ 📄 sobremi.css
┃ ┣ 📄 proyectos.css
┃ ┣ 📄 habilidades.css
┃ ┗ 📄 contacto.css
┗ 📁 public/
┃ ┣ 📁 img/
┗ otros recursos

## 🔄 Proceso de Migración

### 1. 🏗️ De HTML/Bootstrap a Astro
- Se crearon archivos `.astro` para cada página del sitio (`index`, `sobremi`, `proyectos`, `habilidades`, `contacto`).
- Se implementó un **layout base (`Base.astro`)** para reutilizar el encabezado, pie de página y los metadatos en todas las páginas.
- Se reemplazaron los enlaces y scripts locales por **componentes y rutas propias de Astro** (`<Base>`, `/pages/`, `/layouts/`).

### 2. 🎨 De Bootstrap a TailwindCSS
- Se eliminaron las referencias a Bootstrap (`link` de CDN, clases como `container`, `row`, `col`, etc.).
- Se reescribieron los estilos con **clases utilitarias de Tailwind**, como:
  - `flex`, `grid`, `gap`, `text-center`, `rounded-lg`, `shadow-md`, etc.
- Se configuró Tailwind mediante:
  ```bash
  npm install -D tailwindcss
  npx tailwindcss init -p
  Integración en astro.config.mjs:

import { defineConfig } from 'astro/config';
import tailwind from "@astrojs/tailwind";

export default defineConfig({
  integrations: [tailwind()],
});


Importación en src/styles/global.css:

@tailwind base;
@tailwind components;
@tailwind utilities;

### 3. ⚙️ Configuración del proyecto Astro

Se creó el archivo astro.config.mjs con la integración de Tailwind.

Se ajustó el package.json para incluir los scripts:

"scripts": {
  "dev": "astro dev",
  "build": "astro build",
  "preview": "astro preview"
}

### 4. 💅 Estilos adicionales

Se mantuvieron o adaptaron algunos estilos personalizados dentro de los componentes .astro (por ejemplo, animaciones con @keyframes).

Se creó el archivo global.css para reglas generales del sitio.

## ✨ Mejoras Logradas

Rendimiento: Astro genera HTML estático optimizado, lo que mejora la velocidad de carga.

Mantenibilidad: El código está más limpio y modular (componentes separados).

Estilo moderno: Tailwind permite un diseño más flexible y visualmente consistente sin necesidad de clases predefinidas de Bootstrap.

Reutilización: Se centralizó la estructura del sitio en Base.astro, facilitando cambios globales.

## 🧩 Tecnologías Utilizadas

Astro

TailwindCSS

HTML5

CSS3

JavaScript
