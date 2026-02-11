# Ministyle

Ultra-minimal, accessible CSS. Classless-first styling with a small set of utility classes. No JS, no build step.

- **~14 KB** min, ~3 KB gzip · **0 dependencies** · **~208 lines**
- Dark mode (system + toggle) · Golden-ratio typography · WCAG AAA contrast
- CSS-only: tabs, toast, tooltips, accordion · Grid, cards, alerts, badges, pagination, breadcrumbs
- Container queries · Print stylesheet · `prefers-reduced-motion` / `prefers-contrast`

**Looking for a tiny web ecosystem?** See [Minimum Viable Web](https://github.com/Minimum-Viable-Web).

---

## Framework Comparison

| Feature | Ministyle | Tailwind | Bootstrap | Pico | Water.css |
|---------|-----------|----------|-----------|------|-----------|
| Classless HTML styling | ✅ | ❌ | ❌ | ✅ | ✅ |
| Dark mode (auto) | ✅ | ❌ | ❌ | ✅ | ✅ |
| Dark mode (toggle) | ✅ | ✅ | ❌ | ❌ | ❌ |
| Golden ratio typography | ✅ | ❌ | ❌ | ❌ | ❌ |
| CSS-only tabs | ✅ | ❌ | ❌ | ❌ | ❌ |
| CSS-only toast | ✅ | ❌ | ❌ | ❌ | ❌ |
| CSS-only tooltips | ✅ | ❌ | ❌ | ❌ | ❌ |
| CSS-only accordion | ✅ | ❌ | ❌ | ❌ | ❌ |
| Container queries | ✅ | ✅ | ❌ | ❌ | ❌ |
| Grid system | ✅ | ✅ | ✅ | ❌ | ❌ |
| Cards | ✅ | ❌ | ✅ | ❌ | ❌ |
| Alerts | ✅ | ❌ | ✅ | ❌ | ❌ |
| Badges | ✅ | ❌ | ✅ | ❌ | ❌ |
| Pagination | ✅ | ❌ | ✅ | ❌ | ❌ |
| Breadcrumbs | ✅ | ❌ | ✅ | ❌ | ❌ |
| Buttons (sizes) | ✅ | ✅ | ✅ | ❌ | ❌ |
| Form validation states | ✅ | ❌ | ✅ | ✅ | ❌ |
| Compact inline forms | ✅ | ✅ | ✅ | ❌ | ❌ |
| Spacing utilities | ✅ | ✅ | ✅ | ❌ | ❌ |
| Color utilities | ✅ | ✅ | ✅ | ❌ | ❌ |
| Responsive visibility | ✅ | ✅ | ✅ | ❌ | ❌ |
| Loading spinner | ✅ | ❌ | ✅ | ❌ | ❌ |
| Divider with text | ✅ | ❌ | ❌ | ❌ | ❌ |
| Print stylesheet | ✅ | ❌ | ✅ | ❌ | ❌ |
| WCAG AAA contrast | ✅ | ❌ | ❌ | ❌ | ❌ |
| prefers-reduced-motion | ✅ | ✅ | ✅ | ✅ | ✅ |
| prefers-contrast | ✅ | ❌ | ❌ | ❌ | ❌ |
| Skip navigation | ✅ | ❌ | ❌ | ❌ | ❌ |
| Screen reader utility | ✅ | ✅ | ✅ | ❌ | ❌ |

### Size Comparison

| Framework | CSS (min) | CSS (gzip) | Dependencies | Classes |
|-----------|-----------|------------|--------------|---------|
| **Ministyle** | **~15 KB** | **~3 KB** | **0** | **~30 utility + classless** |
| Tailwind CSS | ~300 KB / ~10 KB purged | ~8 KB purged | PostCSS, build | 14,000+ |
| Bootstrap 5 | ~160 KB | ~25 KB | Optional JS | 1,200+ |
| Pico CSS | ~50 KB | ~10 KB | 0 | ~10 |
| Water.css | ~4 KB | ~1.5 KB | 0 | 0 (classless only) |

### Developer Experience

| Aspect | Ministyle | Tailwind | Bootstrap | Pico |
|--------|-----------|----------|-----------|------|
| Learning curve | Near zero | High | Medium | Very low |
| Setup | Drop-in `<link>` | Build config | Optional Sass | Drop-in |
| Customization | 10 CSS variables | tailwind.config | Sass variables | CSS variables |
| JS for components | 0 | N/A | Optional | 0 |
| Best for | Content, docs, a11y | Custom UIs, design systems | Dashboards, enterprise | Simple sites |

---

## Install

**npm:**

```bash
npm install @minimum-viable-web/ministyle
```

**Link in HTML:**

```html
<link rel="stylesheet" href="ministyle.css">
```

**CDN:**

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/Minimum-Viable-Web/ministyle@1.0/ministyle.css">
```

**Copy:** Drop `ministyle.css` into your project (single file, no build).

## Usage

Semantic HTML is styled by default. Add classes only for components or layout.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My page</title>
  <link rel="stylesheet" href="ministyle.css">
</head>
<body>
  <header>
    <nav aria-label="Main"><strong>Site</strong> <a href="/">Home</a></nav>
  </header>
  <main>
    <h1>Hello</h1>
    <p>Content here.</p>
  </main>
</body>
</html>
```

**Dark mode toggle:** Add `class="dark-mode"` or `class="light-mode"` on `<html>`. System preference is used when neither class is set.

## Customization

Override CSS custom properties in your own stylesheet or inline:

- `--bg`, `--text`, `--link`, `--border`, `--card`, `--ok`, `--err`
- `--r` (radius), `--mw` (max-width), `--shadow`

## Demos

- [Kitchen Sink](kitchen-sink.html) — all elements and components
- [Framework comparison](framework-comparison.html) — side-by-side with other frameworks

## Publishing (maintainers)

To publish to npm on each GitHub release:

1. Create an [npm access token](https://www.npmjs.com/settings/~/tokens) (Automation type).
2. In the repo: **Settings → Secrets and variables → Actions** → New repository secret → name `NPM_TOKEN`, value = token.
3. Create a release (e.g. tag `v1.0.0`); the **Publish to npm** workflow will run and publish.

## License

MIT — see [LICENSE](LICENSE).
