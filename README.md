# Cloudflare Waitlist · Landing & Signup

Experimento moderno construido con Astro 5, Tailwind CSS 4 y DaisyUI para validar una lista de espera hospedada en Cloudflare. Incluye una base estilizada mínima y prácticas listas para producción.

## ✨ Características clave

- **Astro Islands** para una carga ultrarrápida y óptima en SEO.
- **Tailwind CSS 4 + DaisyUI** configurados globalmente para crear componentes accesibles.
- **Estructura modular** (`src/client/{components,layouts,pages,styles}`) lista para escalar.
- **Tooling moderno** con Bun para instalaciones y scripts rápidos.

## 🧱 Stack técnico

| Capa      | Detalle                                        |
| --------- | ---------------------------------------------- |
| Runtime   | [Bun](https://bun.sh/) ≥ 1.0                   |
| Framework | [Astro 5](https://docs.astro.build/)           |
| UI        | Tailwind CSS 4 + DaisyUI (tema `dracula`)      |
| Formato   | Prettier + plugins oficiales de Astro/Tailwind |

## 📦 Requisitos previos

- **Node.js 18+** (recomendado para herramientas auxiliares).
- **Bun 1.0+** instalado globalmente (`curl -fsSL https://bun.sh/install | bash`).
- Un navegador moderno para validar la UI.

## 🚀 Guía rápida

```/dev/null/README.md#L23-27
bun install      # instala dependencias
bun dev          # servidor local: http://localhost:4321
bun build        # compila a ./dist listo para producción
bun preview      # sirve la build para QA
```

> Usa `bun astro --help` para explorar comandos adicionales (por ejemplo, `astro add tailwind` si necesitas regenerar la configuración).

## 🗂️ Estructura del proyecto

```/dev/null/README.md#L35-45
cloudflare-waitlist/
├─ public/                 # assets públicos (favicon, imágenes estáticas)
├─ src/
│  └─ client/
│     ├─ components/       # componentes aislados (ej. Hello.astro)
│     ├─ layouts/          # layouts con estilos globales
│     ├─ pages/            # rutas de Astro (index.astro)
│     └─ styles/           # estilos globales + Tailwind config
├─ astro.config.mjs        # configuración principal de Astro
├─ package.json            # scripts y dependencias
└─ bun.lock                # lockfile de Bun
```

## 🎨 Estilos y theming

- `src/client/styles/global.css` importa Tailwind 4 y registra DaisyUI.
- Personaliza temas editando la directiva `@plugin "daisyui"` (p. ej. agrega `themes: [ "dracula", "business" ]`).
- Se recomienda mantener los estilos acoplados a componentes con clases utilitarias y extender solo cuando sea necesario.

## 🧪 Calidad y formato

| Script                 | Acción                                                |
| ---------------------- | ----------------------------------------------------- |
| `bun run format`       | Formatea `src/**/*.{astro,js,ts,css,md}` con Prettier |
| `bun run format:check` | Verifica que el formato sea consistente               |

Integra estos comandos en tu pipeline CI para mantener un estilo uniforme.

## ⚙️ Configuración adicional

1. Copia tus recursos (logos, ilustraciones) a `public/`.
2. Define metadatos en `src/client/layouts/Layout.astro` (título, descripción, OpenGraph).
3. Sustituye `Hello.astro` por tus componentes reales de captura (formularios, hero, etc.).

## 🚢 Despliegue recomendado

- **Cloudflare Pages**: `bun build` + `dist/`.
- **Netlify/Vercel**: usa el adaptador oficial de Astro si necesitas SSR.
- Configura variables de entorno (APIs, claves privadas) mediante los paneles correspondientes; Astro soporta `import.meta.env`.

## 🗺️ Roadmap sugerido

1. Crear componente de formulario con validación (Zod o restricción nativa).
2. Conectar con la API de Cloudflare Workers para almacenar suscripciones.
3. Añadir analítica ligera (PostHog, Plausible).
4. Automatizar pruebas visuales o de accesibilidad (Lighthouse CI).

---

Hecho con Astro, Tailwind y DaisyUI para iterar rápidamente sobre tu lista de espera en Cloudflare. ¡Listo para personalizar y lanzar!
