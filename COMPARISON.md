# Ministyle vs. CSS Frameworks

## Size Comparison

| Framework | CSS Size (min) | CSS Size (gzip) | Dependencies | Classes |
|-----------|---------------|-----------------|--------------|---------|
| **Ministyle** | **~14 KB** | **~3 KB est.** | **0** | **~30 utility + classless** |
| Tailwind CSS | ~300 KB (full) / ~10 KB (purged) | ~8 KB purged | PostCSS, build step | 14,000+ |
| Bootstrap 5 | ~160 KB | ~25 KB | Optional JS (popperjs) | 1,200+ |
| Bulma | ~190 KB | ~26 KB | 0 | 400+ |
| Pico CSS | ~50 KB | ~10 KB | 0 | ~10 (classless-first) |
| Water.css | ~4 KB | ~1.5 KB | 0 | 0 (classless only) |
| MVP.css | ~7 KB | ~2 KB | 0 | 0 (classless only) |
| Simple.css | ~5 KB | ~2 KB | 0 | 0 (classless only) |

## Feature Matrix

| Feature | Ministyle | Tailwind | Bootstrap | Pico | Water.css |
|---------|-----------|----------|-----------|------|-----------|
| Classless HTML styling | Yes | No | No | Yes | Yes |
| Dark mode (auto) | Yes | Manual | Manual | Yes | Yes |
| Dark mode (toggle) | Yes | Yes | No | No | No |
| Golden ratio typography | Yes | No | No | No | No |
| CSS-only tabs | Yes | No | No (JS) | No | No |
| CSS-only toast | Yes | No | No (JS) | No | No |
| CSS-only tooltips | Yes | No | No (JS) | No | No |
| CSS-only accordion | Yes | No | No (JS) | No | No |
| Container queries | Yes | Yes | No | No | No |
| Grid system | Yes | Yes | Yes | No | No |
| Cards | Yes | No (DIY) | Yes | No | No |
| Alerts | Yes | No (DIY) | Yes | No | No |
| Badges | Yes | No (DIY) | Yes | No | No |
| Pagination | Yes | No (DIY) | Yes | No | No |
| Breadcrumbs | Yes | No (DIY) | Yes | No | No |
| Buttons (sizes) | Yes | Yes | Yes | No | No |
| Form validation states | Yes | No | Yes | Yes | No |
| Compact inline forms | Yes | Yes | Yes | No | No |
| Spacing utilities | Yes | Yes | Yes | No | No |
| Color utilities | Yes | Yes | Yes | No | No |
| Responsive visibility | Yes | Yes | Yes | No | No |
| Loading spinner | Yes | No | Yes | No | No |
| Divider with text | Yes | No | No | No | No |
| Print stylesheet | Yes | No | Yes | No | No |
| WCAG AAA contrast | Yes | No | No (AA) | No (AA) | No (AA) |
| prefers-reduced-motion | Yes | Yes | Yes | Yes | Yes |
| prefers-contrast | Yes | No | No | No | No |
| Skip navigation | Yes | No | No | No | No |
| Screen reader utility | Yes | Yes | Yes | No | No |
| Build step required | No | Yes | Optional | No | No |

## Architecture Comparison

### Ministyle
- **Approach**: Classless-first + minimal utility classes
- **Philosophy**: Semantic HTML looks good by default; add classes only for components/layout
- **Learning curve**: Near zero -- write HTML, it looks good
- **Customization**: CSS custom properties (10 tokens control entire theme)
- **JS dependency**: 0 (CSS-only components)
- **Best for**: Content sites, documentation, prototypes, small projects, accessibility-critical apps

### Tailwind CSS
- **Approach**: Utility-first (everything is a class)
- **Philosophy**: Compose design from atomic utilities
- **Learning curve**: High -- must learn utility vocabulary
- **Customization**: tailwind.config.js + build pipeline
- **JS dependency**: Build toolchain required
- **Best for**: Custom designs, SPAs, teams with design systems

### Bootstrap
- **Approach**: Component-first + utilities
- **Philosophy**: Pre-built components for rapid development
- **Learning curve**: Medium -- learn component classes and grid
- **Customization**: Sass variables + overrides
- **JS dependency**: Optional (dropdowns, modals, tooltips need JS)
- **Best for**: Admin panels, dashboards, enterprise apps

### Pico CSS
- **Approach**: Classless-first (closest to Ministyle)
- **Philosophy**: Semantic HTML with minimal classes
- **Learning curve**: Very low
- **Customization**: CSS custom properties
- **JS dependency**: 0
- **Best for**: Simple sites, documentation

## Where Ministyle Wins

1. **Feature density per byte**: ~14 KB delivers grid, cards, tabs, toast, tooltips, badges, alerts, breadcrumbs, pagination, spinner, spacing utilities, dark mode toggle, print stylesheet, and WCAG AAA. No other framework at this size offers this breadth.

2. **Zero JS components**: Tabs, accordion, toast, and tooltips are CSS-only. Bootstrap and Tailwind need JS for these. This means faster load, no JS bundle, and works with JS disabled.

3. **Accessibility by default**: WCAG AAA contrast (14.9:1), visible focus indicators, prefers-reduced-motion, prefers-contrast, skip link, and sr-only utility. Most frameworks target AA at best.

4. **Psychological design grounding**: Golden ratio typography (1.618), Fitts's Law touch targets, Gestalt-informed spacing and grouping. No other minimal framework explicitly applies cognitive science research to its defaults.

5. **No build step**: Drop in a `<link>` tag and write HTML. Tailwind requires PostCSS, Bootstrap's full customization needs Sass.

## Where Others Win

1. **Tailwind**: Unlimited design flexibility for custom UIs. Ministyle's classless approach means you get its aesthetic or you fight it.

2. **Bootstrap**: Massive component library (modals with JS transitions, carousels, offcanvas, scrollspy). Ministyle covers essentials; Bootstrap covers everything.

3. **Pico CSS**: Slightly better classless coverage of edge-case HTML elements. Similar philosophy but 3.5x larger.

4. **Water.css / MVP.css**: Even smaller. If you need nothing beyond styled semantic HTML (no cards, no grids, no components), these are lighter.

## Decision Guide

| If you need... | Use |
|----------------|-----|
| Styled HTML with zero effort | Ministyle or Pico |
| A complete component library | Bootstrap |
| Pixel-perfect custom design | Tailwind |
| Absolute minimum size, no components | Water.css |
| WCAG AAA + psychological design defaults | Ministyle |
| CSS-only interactive components | Ministyle |
| Complex JS-driven components | Bootstrap + JS |
| Team with existing Tailwind knowledge | Tailwind |
