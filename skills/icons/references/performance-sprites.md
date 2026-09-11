# Symbol Sprites

For many repeated icons, reduce duplicate path markup with sprites:

```html
<!-- Define once, hidden -->
<svg xmlns="http://www.w3.org/2000/svg" style="display:none" aria-hidden="true">
  <symbol id="icon-search" viewBox="0 0 24 24">
    <path d="..."/>
  </symbol>
  <symbol id="icon-menu" viewBox="0 0 24 24">
    <path d="..."/>
  </symbol>
</svg>

<!-- Use anywhere -->
<svg aria-hidden="true" focusable="false" width="20" height="20">
  <use href="#icon-search"/>
</svg>
```

External sprites (`<use href="/icons.svg#search"/>`) need a polyfill or bundler inlining on older Safari builds that block cross-origin fragment references.

# Performance

Relative cost pattern (many repeated icons):

- Optimized inline SVG or component imports: good default for app UI
- Symbol sprite: good when the same glyphs repeat often in one document
- Full icon-font / mega-pack imports: avoid unless tree-shaken to used glyphs

## Recommendations

- Tree-shake modern SVG icon libraries (Lucide, Heroicons, Phosphor, and similar).
- Import only the icons you use; do not load a 1MB+ font or full pack for ten glyphs.
- Inline critical above-the-fold icons; lazy-load larger sprite sheets for secondary chrome.
- Prefer SVG over icon fonts unless a documented legacy browser constraint requires fonts.
