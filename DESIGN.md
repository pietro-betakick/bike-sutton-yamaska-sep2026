# DESIGN.md — Trip brief visual system

Mode: Operate (plan + navigate). Light ambient for outdoor phone glare.

## Stack (open source, high GitHub stars — verify periodically)
| Library | Role | Why |
|---|---|---|
| [Leaflet](https://github.com/Leaflet/Leaflet) | Map | ~45k★, battle-tested mobile maps |
| [Pico CSS](https://github.com/picocss/pico) | Layout / forms / type | ~17k★, class-light semantic HTML |
| [Lucide](https://github.com/lucide-icons/lucide) | Icons | ~25k★, consistent stroke icons |
| OpenStreetMap / CARTO / Esri tiles | Basemap | Public tiles; prefer CARTO Voyager or Esri World Topo |

Do not invent CSS frameworks. Prefer CDN builds pinned by major version.

## Type
- UI sans: system-ui stack with `"Segoe UI", system-ui, sans-serif` (no decorative display face for operate mode)
- Body measure ~65–75ch
- Clear weight steps: page title, section h2, body, muted meta

## Color
- Ink `#1a1a1a`, muted `#5c5c5c`, paper `#f7f6f2`, card `#ffffff`
- Day 1 track `#0b6e4f`, Day 2 `#1b4965`, accent link `#0b6e4f`
- Warn surface warm cream; success soft green. Contrast ≥4.5:1 for body text.

## Layout
- Single column, max-width ~52rem
- Map full-bleed within column, min-height 420px
- Tables for day numbers; hotel picks as simple bordered blocks, not nested card stacks
- No kicker/eyebrow labels above headings
- No gradient text, no glass decoration, no emoji icons

## Motion
One subtle map fade-in or legend settle max. No scroll-jacking.

## Components
- Chip row for Day / Night / Style facts
- Day section with km, climb, overnight
- Download list with `download` attribute on GPX links
- Footer: trip name, dates, tile attribution
