Create html artifacts using the following guidelines:
## Brand
- Name: `Brand Name`
- Logo: `files/logo.svg` (light) / `files/logo-dark.svg` (dark)
- Tone: clear, direct, professional

## Colors
Define them as CSS tokens on `:root`:

| Token | Value | Use |
|---|---|---|
| `--color-primary` | `#1A2B4C` | Headers, main accents |
| `--color-secondary` | `#3C7DD9` | Links, highlights |
| `--color-accent` | `#F2A900` | Callouts, key figures |
| `--color-bg` | `#FFFFFF` | Background |
| `--color-surface` | `#F5F6F8` | Cards, tables |
| `--color-text` | `#1F1F1F` | Body text |
| `--color-muted` | `#6B7280` | Captions, secondary text |

## Typography
- Headings: `Heading Font`, fallback `sans-serif`
- Body: `Body Font`, fallback `sans-serif`
- Numbers: tabular figures (`font-variant-numeric: tabular-nums`)
- Sizes: H1 40px / H2 28px / H3 20px / body 16px

## Layout
- One idea per slide
- Generous whitespace, 8px spacing scale
- Max content width: 1200px
- Works on mobile (16px side gutter, no horizontal scroll)

## Components
- **Title slide**: logo, title, subtitle, date
- **Section divider**: primary background, white title
- **KPI tiles**: big number, short label, optional delta
- **Tables**: surface background header, no vertical borders
- **Charts**: brand colors in token order, no 3D, no pie charts with more than 4 slices

## Don'ts
- Don't mix more than 2 fonts
- Don't use colors outside the palette
- Don't stretch or recolor the logo
