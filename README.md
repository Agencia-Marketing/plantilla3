# Plantilla 3 — Cyber-Luxe Glassmorphism Agency

Landing page Cyber-Luxe Glassmorphism para agencia de marketing digital. Rediseño visual radical de Plantilla 1 — mismo contenido, estética de cristal esmerilado y void cósmico.

## Stack

- **[Astro](https://astro.build)** v5 — Static site generator
- **[Tailwind CSS](https://tailwindcss.com)** v3 — Utility-first CSS
- **[PostCSS](https://postcss.org)** + Autoprefixer
- **[Cloudflare Pages](https://pages.cloudflare.com)** — Hosting
- **Sora + Mulish** — Tipografías premium (Google Fonts)
- **Material Symbols** — Iconografía

## Estética

- Fondo void negro (`#03030F`) con mesh gradients indigo-violeta-rosa
- Tarjetas de cristal: `backdrop-filter: blur(20px) saturate(180%)`
- Bordes luminosos 1px: `rgba(255,255,255,0.075)` → `rgba(0,240,255,0.28)` en hover
- Sombras glass: `0 8px 32px rgba(0,0,0,0.50)` + `inset 0 1px 0 rgba(255,255,255,0.05)`
- Acento eléctrico cyan (`#00F0FF`) + violeta suave (`#A78BFA`)
- Micro-interacciones: magnetic buttons, reveal/stagger-fade en scroll, float animations

## Empezar

```bash
npm install
npm run dev       # → localhost:4321
npm run build     # → dist/
npm run preview
```

## Personalizar

### Colores (cambiar en 2 lugares)

**1. `src/styles/global.css` → bloque `:root`:**
```css
:root {
  --accent:      #00F0FF;  /* Cyan eléctrico (interactivo) */
  --accent-2:    #A78BFA;  /* Violeta suave (secundario) */
  --bg-void:     #03030F;  /* Fondo void base */
  --grad-indigo: #4F46E5;  /* Mesh gradient A */
  --grad-violet: #7C3AED;  /* Mesh gradient B */
  --grad-pink:   #DB2777;  /* Mesh gradient C */
}
```

**2. `tailwind.config.mjs` → `theme.extend.colors`:**
```js
colors: {
  'accent':    '#00F0FF',
  'accent-2':  '#A78BFA',
  'bg-void':   '#03030F',
  'bg-depth':  '#08082A',
}
```

### Tipografía
En `src/layouts/Layout.astro` y `html/*.html`, reemplazar el link de Google Fonts y las familias `font-display` / `font-body` en CSS.

## Servicios (9 páginas)

| Ruta | Servicio |
|---|---|
| `/servicios/desarrollo-web` | Desarrollo Web |
| `/servicios/agentes-ia` | Agentes de IA |
| `/servicios/diseno-grafico` | Diseño Gráfico |
| `/servicios/redes-sociales` | Gestión de Redes |
| `/servicios/campanas-publicitarias` | Campañas de Ads |
| `/servicios/videomarketing` | Videomarketing |
| `/servicios/embudos-venta` | Embudos de Venta |
| `/servicios/creadores-ugc` | Creadores UGC |
| `/servicios/creacion-contenido` | Creación de Contenido |

## Versión HTML standalone

La carpeta `html/` contiene versiones HTML puras (Tailwind CDN + CSS inline) sin build. Abrir directamente en navegador o con Live Server.

## Deploy

```bash
git push  # → Cloudflare Pages build automático
```
