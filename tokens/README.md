# Tokens

Variables del sistema de diseño Cirkular Origin en formato CSS y JSON.

## Archivos

| Archivo | Contenido |
|---|---|
| `colors.css` | Paleta completa (forest scale, brand, semánticos, gradientes, transparencias) |
| `typography.css` | Familias, tamaños, pesos, leading, tracking + clases utilitarias (`.co-h1`, `.co-body`, etc.) |
| `spacing.css` | Grid 4-pt, padding, gutters, radii, contenedores máximos |
| `elevation.css` | Shadows, glow lime, borders, blur |
| `animation.css` | Easings, duraciones, escalas de press (con soporte `prefers-reduced-motion`) |
| `index.css` | Importa todos los anteriores |
| `tokens.json` | Mismas variables en formato W3C Design Tokens (para Figma plugins, Style Dictionary, herramientas de diseño) |

## Uso en CSS / React / Vue

```css
@import "https://raw.githubusercontent.com/CirkularAgroFintech/cirkular-origin/main/tokens/index.css";

.button {
  background: var(--co-lime);
  color: var(--co-forest-900);
  padding: var(--co-space-3) var(--co-space-6);
  border-radius: var(--co-radius-pill);
  transition: transform var(--co-duration-hover) var(--co-ease-out);
}
```

## Uso en Tailwind

Mapear en `tailwind.config.js`:

```js
module.exports = {
  theme: {
    extend: {
      colors: {
        forest: { 900: "#1A2B2D", 800: "#23393B", 700: "#2E4A4D" },
        lime: "#C7FF00",
        teal: "#05C0CA",
        purple: "#7A00FF",
        cream: "#F4F1EA",
      },
      fontFamily: {
        sans: ["Plus Jakarta Sans", "system-ui", "sans-serif"],
        serif: ["Fraunces", "Georgia", "serif"],
      },
      borderRadius: {
        lg: "20px",
        xl: "28px",
        "2xl": "36px",
      },
    },
  },
};
```

## Uso con Style Dictionary

`tokens.json` cumple el formato W3C de Design Tokens — se puede transformar a iOS (Swift), Android (XML), Flutter (Dart), JS, etc., con [Style Dictionary](https://amzn.github.io/style-dictionary/) o [Tokens Studio](https://tokens.studio/).

## Reglas críticas

- **Lima reservado** a CTA primario y KPI hits. Nunca como fondo grande.
- **Nunca lima sobre blanco** (falla contraste).
- **Forest 900/800** es home base — depth con tint shifts, no con shadows.
- Numéricas financieras: aplicar `.co-tabular` para `font-variant-numeric: tabular-nums`.
