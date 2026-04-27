# Cirkular Origin — Design System

> A shareable, copy-pasteable summary of the Cirkular Origin design system. Hand this to teammates, contractors, or partners who need to ship work that looks and sounds like Cirkular Origin without spelunking the full repo.

---

## 1. About Cirkular Origin

**Cirkular Origin** is an agro-regenerative investment platform connecting visionary smallholder coffee producers with purpose-driven investors through transparent carbon-credit financing.

Three product surfaces:

| Surface | Audience | Purpose |
|---|---|---|
| Investor web app | Purpose-driven investors, funds | Browse origins, fund coffee plots, track impact + carbon credits |
| Producer mobile app | Smallholder coffee farmers (LatAm focus) | Onboarding, subscription tiers, regional selection, activity logging, progress dashboard |
| Marketing site / dashboards | Public, partners | Brand storytelling, transparency reports |

---

## 2. Brand voice

**In three words:** Clear. Simple. Inspiring.

Optimistic and empowering. Celebrates the dignity of rural work and regenerative agriculture without being saccharine. Treats producers and investors as adults — no jargon, no greenwashing, no "save the planet" hype.

### Tone dials

| Dial | Where it sits |
|---|---|
| Formal ↔ Casual | Mid-casual — investor-grade, but warm |
| Plain ↔ Poetic | Plain by default; serif italic accents for impact |
| Calm ↔ Energetic | Calm-confident — lime is loud, words don't have to be |
| Modest ↔ Bold | Quietly bold — numbers carry the weight |

### Pronouns & POV

- **"You"** for the reader (investor or producer). Always.
- **"We"** for Cirkular Origin as an organisation, sparingly. Avoid "we believe…" filler.
- **Names** for producers — never "the farmer." Use first names + region (e.g. "Doña Marta, Huehuetenango").

### Casing rules

- **Sentence case** for every UI label, button, header, and headline.
  ✅ "Fund this origin" — not "Fund This Origin"
- **Title Case** only for proper nouns and the product name: *Cirkular Origin*.
- **UPPERCASE** only for tight micro-labels (eyebrows, status pills, table headers) — `letter-spacing: 0.12em`.

### Numbers, units, money

- Tabular figures everywhere financial. `font-variant-numeric: tabular-nums`.
- Currency: `$1,240` for USD; `€` for Euro displays — never spell out.
- Carbon: `1.2 tCO₂e` (lowercase t, subscript 2 e).
- Percent: `+12.4%` — sign first, no space.

### Emoji & exclamation

- **No emoji in product UI.** (Rare exception: marketing moments.)
- Exclamation marks: at most one per screen, only on success states ("Funded!").

### What we don't say

- ❌ "Game-changing", "revolutionary", "disruptive"
- ❌ "Sustainable" used as a magic word — be specific (regenerative, agroforestry, shade-grown)
- ❌ "Farmers" alone — say "smallholder producers" or use names
- ❌ "Eco-friendly", "green" as adjectives for the product

### Example copy

> **Hero (marketing):**
> Coffee that pays its own way home.
> Fund the regenerative practices of smallholder producers — and earn verified carbon credits as the trees grow.
>
> **CTA:** Browse origins
>
> **Empty state:** No origins funded yet. Pick one that moves you — every plot tells you exactly what your capital does.
>
> **Producer push:** Your soil sample arrived in the lab. We'll have results in 6 days.
>
> **Error:** Couldn't load this origin. Check your connection and try again.

---

## 3. Color

The system is **dark-first**: deep forest green is home base, lime is the spark.

### Brand core

| Token | Hex | Role |
|---|---|---|
| `--co-forest-900` | `#1A2B2D` | Primary background |
| `--co-forest-800` | `#23393B` | Surface · cards · navs |
| `--co-lime` | `#C7FF00` | Accent · CTA · KPI hits |
| `--co-teal` | `#05C0CA` | Brand · data viz secondary · links |
| `--co-purple` | `#7A00FF` | Brand · tertiary accent |
| `--co-white` | `#FFFFFF` | On-dark text |
| `--co-cream` | `#F4F1EA` | Light background · print |

### Forest scale

`#131614` · `#1A2B2D` · `#23393B` · `#2E4A4D` · `#3C5C5F` · `#547073`

### Semantic

| Role | Hex |
|---|---|
| Success | `#6BD96E` |
| Warning | `#FFB347` |
| Danger | `#FF5C5C` |
| Info | `#05C0CA` (teal) |

### Rules

- **Lime is reserved.** ~3–5 % of pixels per screen. Never as a large fill. Lime fills are for primary CTAs and KPI hits only.
- **Purple/teal appear together only as the logo gradient** or in decorative hero moments. Never split into a 50/50 layout.
- **Combinations:** white on forest · forest on cream · forest on lime. **Never lime on white** (fails contrast and looks toxic).

### Brand gradients

- **Spiral:** `linear-gradient(160deg, #7A00FF 0%, #4A35E0 35%, #05C0CA 65%, #C7FF00 100%)` — logo-derived, hero accents only.
- **Lime:** `linear-gradient(140deg, #C7FF00 0%, #9FE600 100%)` — CTA hover, KPI fill.
- **Forest:** `linear-gradient(180deg, #23393B 0%, #1A2B2D 100%)` — card depth on dark.

---

## 4. Typography

- **Plus Jakarta Sans** — full weight range, used for body, UI, headings, numerics. (Brand fonts shipped locally in `fonts/`.)
- **Fraunces italic** — editorial accent only. *Placeholder for the real "cirkular" wordmark serif — replace if/when licensed.*
- **No third family.** Mono (JetBrains Mono) is rare — reserved for code/keys.

### Hierarchy

| Style | Size | Weight | Tracking | Use |
|---|---|---|---|---|
| Display | 88 | 800 | -2 % | Marketing hero only |
| H1 | 64 | 800 | -2 % | Section headlines |
| H2 | 48 | 700 | -1 % | Page titles |
| H3 | 36 | 600 | -1 % | Card / module titles |
| H4 | 28 | 600 | snug | Subsections |
| Body | 16 | 400 | normal · 1.65 line-height | Long form |
| Body sm | 14 | 400 | 1.5 line-height | Secondary |
| Eyebrow | 12 | 600 | 0.12 em UPPERCASE · lime | Section markers |
| Caption | 12 | 400 | 1.4 line-height | Metadata |

### Numerics

Use tabular figures everywhere financial. Prefer `font-variant-numeric: tabular-nums` and `font-feature-settings: "tnum"`.

---

## 5. Spacing, radii, elevation

### Spacing — 4-pt grid

`4 · 8 · 12 · 16 · 20 · 24 · 32 · 40 · 48 · 64 · 80 · 96`

- Section padding: 96 px desktop, 56 px mobile.
- Card padding: 24 px default, 32 px on hero modules.
- Side gutter: 24 px mobile, 48 px desktop.

### Radii

| Token | px | Use |
|---|---|---|
| xs | 6 | Inline tags |
| sm | 10 | Small inputs |
| md | 14 | Inputs / pills |
| lg | 20 | **Cards (default)** |
| xl | 28 | Modals, hero modules |
| 2xl | 36 | Phone bezels, large containers |
| pill | 999 | Primary buttons, pills |

### Elevation

- Default elevation on dark surfaces is **none** — depth comes from tint shifts (`forest-900` → `forest-800` → `forest-700`).
- Drop shadows reserved for popovers and modals (`shadow-3 = 0 14px 40px rgba(10,18,19,0.45)`).
- Hero/highlight effect: **lime glow ring** — `0 0 0 1px rgba(199,255,0,0.35), 0 10px 30px rgba(199,255,0,0.18)`. Use sparingly on the focused KPI or active timeline node.

### Borders & dividers

- 1 px hairlines at `rgba(255,255,255,0.10)` on dark, `rgba(35,57,59,0.12)` on light.
- Strong borders only on focus rings: 2 px lime + lime glow.
- No gray boxes — surfaces are tinted forest, not neutral.

---

## 6. Visual foundations

### Backgrounds & imagery

- **Photography is warm and earthy** — green canopy, red coffee cherries, wet soil, weathered hands. Slight grain. Never over-saturated. **Never** stock-y "happy farmer with thumbs up."
- **Full-bleed photography** is allowed in marketing heroes. In-app, photography sits inside rounded containers (20–28 px radius) and pairs with a 0–60 % forest-900 gradient overlay for legibility.
- **Decorative pattern:** the spiral mark from the logo can be enlarged to ~150 % of its container as a watermark (10 % opacity, lime or teal) on dark hero panels. Do not tile it.
- **No abstract gradients as backgrounds.** The spiral gradient is logo-specific, not wallpaper.

### Animation

- **Easing:** `cubic-bezier(0.22, 1, 0.36, 1)` (ease-out) for everything entering. `cubic-bezier(0.34, 1.56, 0.64, 1)` (gentle spring) only on the lime CTA press release.
- **Durations:** 140 ms hovers/toggles · 220 ms component transitions · 420 ms page reveals.
- **Hover (dark):** background lifts to +3 % white. **Lime CTAs:** brightness 1.06, no color shift.
- **Press:** scale 0.98 + 80 ms. Lime CTA: scale 0.97 + 60 ms.
- **Fades** are the default. Bounce/elastic is forbidden except the spring above.
- **Loaders:** slow 1.4 s spinning spiral (logo mark, lime tint).
- **Charts** animate value-in on mount only; never on hover.

### Layout rules

- Sticky top bar (web): 64 px, `forest-800`, hairline border.
- Mobile bottom tab bar: 80 px, `forest-800`, lime indicator as a 4 px pill behind the active label.
- Max content width: 1200 px dashboards · 960 px editorial.
- Fixed elements use `shadow-2` only when content scrolls under them.

### Transparency & blur

- Used **rarely**. Blur reserved for the modal scrim (`backdrop-filter: blur(12px)` over `rgba(15,25,26,0.72)`).
- No glassmorphism navs.
- Avoid stacking translucent layers — flatten to a tinted surface instead.

### Cards

- Background: `forest-800` (or translucent on photo).
- Radius: 20 px.
- Border: 1 px `rgba(255,255,255,0.10)` only when on a busy background.
- No shadow at rest. Hover lifts background tint (no transform).
- Padding: 24 px. Title sits on its own line, eyebrow above.

---

## 7. Iconography

- **Primary set:** Lucide-aligned, 1.5 px stroke, rounded join + cap. (Use `https://unpkg.com/lucide@latest/dist/umd/lucide.js` until a custom set ships.)
- **Brand glyph:** the spiral S-mark is treated as an icon — used standalone in app shells, loaders, favicon.
- **Filled status icons** for success / warning / danger pills only.
- **No emoji** in product UI.
- **No unicode pictographs** as functional icons (no ✓ ✗ → in copy).
- **No PNG/raster icons** — everything vector.

---

## 8. Logo & assets

Available in `assets/` (PNG):

- `logo-mark.png` — spiral mark only, transparent BG
- `logo-landscape-dark.png` / `logo-landscape-light.png` — horizontal lockup
- `logo-portrait-dark.png` / `logo-portrait-light.png` — vertical lockup
- `logo-horizontal-light.png` — horizontal on light only
- `logo-green.png` / `logo-white.png` — solid single-colour wordmarks
- `logo-wordmark.png` — wordmark only (no mark)
- `logo-landscape-*-gs.png` — grayscale variants for print

**Rules:** Always on dark forest or white/cream backgrounds. Never on photography without a forest capsule behind it. Maintain clear-space equal to the height of the spiral mark on all sides.

---

## 9. Components — quick reference

### Buttons

| Variant | Background | Text | Use |
|---|---|---|---|
| Primary | `#C7FF00` | `#1A2B2D` | The one CTA per screen |
| Secondary | transparent · 1 px white-28 border | `#FFFFFF` | Tertiary actions |
| Ghost | `rgba(255,255,255,0.06)` | `#FFFFFF` | Toolbar, inline |
| Danger | `#FF5C5C` | `#FFFFFF` | Destructive |

Default radius: **999 (pill)**. Padding: 12 × 22 (md), 8 × 14 (sm).

### Inputs

- Background: `rgba(255,255,255,0.04)`
- Border: 1 px `rgba(255,255,255,0.10)` → focus: 1 px lime + 3 px lime glow
- Radius: 12 px · Padding: 12 × 14
- Placeholder: `rgba(255,255,255,0.35)`

### Pills & badges

- Status pills use 14 % tint of their semantic colour as background, full colour for text + 6 px dot.
- Brand pill: solid lime + forest text.
- Tags: `rgba(255,255,255,0.06)` background, 11 px UPPERCASE.

### Progress

- Bars: 8 px tall, `rgba(255,255,255,0.08)` track, lime fill (or teal→lime gradient for carbon).
- Rings: 3 px stroke, rounded cap, lime arc on `rgba(255,255,255,0.10)` track.

---

## 10. Files in the repo

```
/
├─ README.md                 — full spec (this is its TL;DR)
├─ DESIGN.md                 — this file (shareable summary)
├─ SKILL.md                  — Agent Skill entrypoint
├─ colors_and_type.css       — all design tokens (CSS variables)
├─ fonts/                    — Plus Jakarta Sans (variable + statics)
├─ assets/                   — logo set (PNGs)
├─ preview/                  — design-system tab cards
└─ ui_kits/
   ├─ web/                   — investor dashboard (React/JSX)
   └─ mobile/                — producer app (React/JSX)
```

---

## 11. Caveats & open questions

- The original brand PDF (`2022.05.19 CIRKULAR BRAND.pdf`) was referenced but never delivered. Some details (clear-space rules, exact wordmark font, photographic guidelines) are interpreted from logo PNGs + written notes. **Re-upload to lock these.**
- The "cirkular" wordmark is a custom or licensed serif italic — Fraunces italic is a placeholder. **Send the real font file** if you have it.
- No codebase or Figma was provided — UI kits are interpretations, not recreations. Replace with real sources when available.
- Iconography is hand-drawn, Lucide-aligned. Swap for a production icon set when one exists.
- Photography in the web kit uses Unsplash placeholders. Replace with real producer imagery.
- Spanish copy in the mobile kit is illustrative — needs native review.

---

*Maintained alongside `colors_and_type.css` and the UI kits in this project. When tokens change, update both.*
