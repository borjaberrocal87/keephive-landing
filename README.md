# KeepHive Landing

Landing page estática para [KeepHive](https://github.com/keephive/keephive) — AI Agent for Discord Communities.

Sitio web institucional que explica el producto, documentación de hosting y enlace al repositorio de GitHub.

## Stack Tecnológico

| Capa | Tecnología |
|------|------------|
| Framework | [Astro](https://astro.build/) (SSG) |
| UI Components | React 18 (islands) |
| Styling | [Tailwind CSS](https://tailwindcss.com/) |
| Animations | [Framer Motion](https://www.framer.com/motion/) |
| Icons | [Lucide React](https://lucide.dev/) |
| Typography | Inter, Space Grotesk, JetBrains Mono |
| Hosting | [Cloudflare Pages](https://pages.cloudflare.com/) |
| CI/CD | GitHub Actions |

## Inicio Rápido

### Requisitos

- Node.js `20.19.0` o superior
- npm o yarn

### Instalación

```bash
# Clonar el repositorio
git clone https://github.com/borjaberrocal87/keephive-landing.git
cd keephive-landing

# Instalar dependencias
npm install
```

### Desarrollo

```bash
# Iniciar servidor de desarrollo
npm run dev

# Abrir en el navegador
open http://localhost:4321
```

### Build

```bash
# Generar sitio estático
npm run build

# Vista previa del build
npm run preview
```

## Estructura del Proyecto

```
.
├── public/                    # Assets estáticos
│   ├── favicon.ico
│   ├── og-image.png          # 1200x630 para social sharing
│   ├── robots.txt
│   └── sitemap.xml
├── src/
│   ├── components/            # Componentes Astro y React
│   │   ├── Header.astro
│   │   ├── Hero.astro
│   │   ├── Features.astro
│   │   ├── HowItWorks.astro
│   │   ├── Installation.astro
│   │   ├── Comparison.astro
│   │   ├── Footer.astro
│   │   ├── CodeBlock.tsx      # React island
│   │   ├── ThemeToggle.tsx    # React island
│   │   └── MobileMenu.tsx     # React island
│   ├── layouts/
│   │   └── BaseLayout.astro
│   ├── pages/
│   │   ├── index.astro
│   │   └── changelog.astro
│   ├── styles/
│   │   └── global.css
│   └── content/
│       └── docs/              # Contenido Markdown
├── astro.config.mjs
├── tailwind.config.mjs
├── tsconfig.json
└── package.json
```

## Despliegue

### Cloudflare Pages (Recomendado)

1. Conectar el repositorio GitHub a Cloudflare Pages
2. Configurar:
   - **Build command:** `npm run build`
   - **Build output directory:** `dist`
   - **Node.js version:** 20
3. Configurar dominio personalizado en Cloudflare DNS

### Vercel

1. Importar repositorio en Vercel
2. Framework: Astro
3. Configurar dominio personalizado

### GitHub Pages

```bash
# El deploy automático está configurado en .github/workflows/deploy.yml
# Se ejecuta automáticamente al hacer push a main
```

## Configuración de Dominio

### DNS Records (Cloudflare Pages)

```
Type    Name    Value                   TTL
A       @       76.76.21.21            300
CNAME   www     keephive.pages.dev     300
```

## Métricas de Performance

| Métrica | Target |
|---------|--------|
| Lighthouse Performance | ≥ 95 |
| First Contentful Paint | < 1s |
| Largest Contentful Paint | < 2.5s |
| Cumulative Layout Shift | < 0.1 |
| Lighthouse SEO | 100 |
| Lighthouse Accessibility | ≥ 95 |

## Características

- **Dark mode** con toggle en el header
- **Header sticky** que se mantiene al hacer scroll
- **Smooth scroll** para links internos
- **Animaciones sutiles** al hacer scroll (fade-in)
- **Syntax highlighting** en bloques de código
- **Menú responsive** para móvil
- **SEO optimizado** (meta tags, JSON-LD, sitemap)
- **Accesible** (WCAG 2.1 AA)

## Documentación

- [PRD de la Landing](context/PRD.md)
- [Estándares Frontend](docs/frontend-standards.md)
- [Guía de Desarrollo](docs/development_guide.md)

## Licencia

MIT License - Ver [LICENSE](LICENSE)

---

**KeepHive** — AI Agent for Discord Communities
