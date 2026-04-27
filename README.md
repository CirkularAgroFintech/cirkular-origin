# Cirkular Origin

Repositorio central del **sistema de diseño y activos de marca** de Cirkular Origin — la plataforma agro-regenerativa que conecta productores cafeteros con inversionistas a través de financiamiento por créditos de carbono.

## Contenido

| Carpeta / archivo | Descripción |
|---|---|
| [`DESIGN.md`](./DESIGN.md) | Sistema de diseño completo: colores, tipografía, spacing, componentes, voz de marca |
| [`tokens/`](./tokens/) | Tokens en CSS (`.css`) y W3C Design Tokens (`.json`) — listos para importar en código |
| [`brand/`](./brand/) | PDFs originales de marca (2022): identidad y cultura |
| [`assets/logos/`](./assets/logos/) | Logos oficiales de Cirkular Origin (PNG en variantes landscape/portrait, dark/bright, color/grayscale) |
| [`assets/logos-source/`](./assets/logos-source/) | Variantes históricas y alternativas de logo |
| [`assets/icons/`](./assets/icons/) | Set de iconos custom de Cirkular (zip) |
| [`assets/source/`](./assets/source/) | Archivos editables originales (`.ai`, `.cdr`) — abrir con Adobe Illustrator / CorelDraw |

## Uso rápido

- Para **copy y tono**: ver sección 2 de `DESIGN.md`
- Para **paleta de colores y tokens**: ver sección 3
- Para **tipografía**: ver sección 4
- Para **componentes UI**: ver sección 9
- Para **logos**: usar archivos en `assets/logos/` — respetar área de protección y combinaciones permitidas

## Reglas críticas

- ❌ **Nunca** lima sobre blanco (falla contraste)
- ❌ **Nunca** logo sobre fotografía sin cápsula forest detrás
- ❌ **Nunca** usar emoji en producto UI
- ✅ Sentence case en TODO label, botón, título
- ✅ Lima reservado para CTA primario (~3-5% de píxeles por pantalla)
- ✅ Tabular figures en cifras financieras

## Mantenimiento

Cualquier cambio a tokens debe reflejarse en `DESIGN.md` y en `colors_and_type.css` (cuando exista en el repo de implementación).

---

© Cirkular Agro Fintech S.A.S.
