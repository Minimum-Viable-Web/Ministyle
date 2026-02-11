# Ministyle

Ultra-minimal, accessible CSS. Classless-first styling with a small set of utility classes. No JS, no build step.

- **~14 KB** min, ~3 KB gzip · **0 dependencies** · **~208 lines**
- Dark mode (system + toggle) · Golden-ratio typography · WCAG AAA contrast
- CSS-only: tabs, toast, tooltips, accordion · Grid, cards, alerts, badges, pagination, breadcrumbs
- Container queries · Print stylesheet · `prefers-reduced-motion` / `prefers-contrast`

## Install

**Link in HTML:**

```html
<link rel="stylesheet" href="ministyle.css">
```

**CDN (replace `owner/repo` with your fork or the canonical repo):**

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/owner/repo@1.0/ministyle.css">
```

**Optional:** Copy `ministyle.css` into your project (single file, no build).

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

**Dark mode toggle:** Add `class="dark-mode"` or `class="light-mode"` on `<html>` (e.g. via a button that toggles the class). System preference is used when neither class is set.

## Customization

Override CSS custom properties in your own stylesheet or inline:

- `--bg`, `--text`, `--link`, `--border`, `--card`, `--ok`, `--err`
- `--r` (radius), `--mw` (max-width), `--shadow`

## Demos

- [Kitchen Sink](kitchen-sink.html) — all elements and components
- [Framework comparison](framework-comparison.html) — side-by-side with other frameworks

## License

MIT — see [LICENSE](LICENSE).
