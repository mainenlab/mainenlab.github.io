# Site Template

`page.html` is the canonical style template for mainenlab.org. Copy it to start any new page.

## Placeholders

Replace these HTML comments with actual content:

| Placeholder | Where | What |
|:--|:--|:--|
| `<!-- TITLE -->` | `<title>` tag | Page title (appears before " — Mainen Lab") |
| `<!-- DESCRIPTION -->` | `<meta>` tag | One-line summary for search engines / link previews |
| `<!-- HEADER -->` | Inside `header h1` | Page heading |
| `<!-- SUBTITLE -->` | Inside `header .subtitle` | Secondary line (e.g. "Champalimaud Foundation, Lisbon") |
| `<!-- CONTENT -->` | Between `</header>` and `<footer>` | Page body — use `.page` (700px prose), `.page-wide` (920px layouts), or custom |
| `<!-- FOOTER -->` | Right side of footer separator | Additional footer links (left side is always "mainenlab.org") |

## Identity

- **Palette**: warm off-white light mode (`#fafaf8`) / near-black dark mode (`#111111`), toggled via `data-theme` attribute
- **Accent**: teal (`#0d9488` light, `#2dd4bf` dark) — used for links, pills, active states
- **Typography**: system font stack (`-apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif`), tight negative letter-spacing on headings, `font-weight: 600` headings
- **Favicon**: teal circle with white "ML" monogram (`favicon.svg`)
- **Border radius**: `8px` for cards, `6px` for inputs/buttons, `999px` for pills
- **Shadows**: subtle (`0 1px 3px rgba(0,0,0,0.06)` light, `0.3` dark)

## Typography quick reference

| Role | Style | Usage |
|:--|:--|:--|
| Page title | 1.5rem, weight 600, -0.02em tracking | `h1` |
| Section heading | 1.15rem, weight 600 | `h2` |
| Subsection | 0.95rem, weight 600 | `h3` |
| Body text | 1rem, weight 400, 1.6 line-height | `p`, `.card-body` |
| Subtitle | 0.95rem, muted color | `.subtitle` |
| Section label | 0.72rem, uppercase, 0.08em tracking | `.section-title` |
| Meta text | 0.78-0.88rem, muted | `.page-meta`, `.card-span` |

## Available components

- **`.container`** / **`.page`** / **`.page-wide`** — centered containers (920px / 700px / 920px)
- **`.card`** / **`.card-grid`** — white cards with subtle shadow, auto-fill grid
- **`.pill`** — rounded filter pill (border-only default, filled `.active` state)
- **`.status`** — uppercase badge (`.active` green, `.completed` gray, `.dormant` yellow)
- **`.callout`** — left-bordered accent block
- **`.pub-list`** — publication list styling
- **`.search-box`** — full-width search input
- **`.links`** — horizontal link row
- **`.back`** — left-arrow back link ("&larr; Mainen Lab")

## Theme toggle

The dark/light toggle is built in. It reads from `localStorage('theme')` on load and persists user preference. The toggle button lives inside `<header>` as a positioned element.

## Rules

- All CSS is inline in `<style>`. No external stylesheets, no frameworks.
- No external font dependencies — system font stack only.
- Dual-theme via CSS custom properties on `:root` / `[data-theme="dark"]`.
- Colors reference custom properties, never hardcoded (except status badge colors).
- Responsive breakpoint at 640px.
- Favicon path assumes root-level; use `../favicon.svg` for subdirectory pages.
