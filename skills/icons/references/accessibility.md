# Icon Accessibility Patterns

**Decorative icons (next to visible text):**

```html
<button>
  <svg aria-hidden="true" focusable="false" width="20" height="20">...</svg>
  Save
</button>
```

**Informative icons (standalone, no visible label):**

```html
<button type="button" aria-label="Save document">
  <svg aria-hidden="true" focusable="false" width="20" height="20">...</svg>
</button>

<!-- Or with visually hidden text -->
<button type="button">
  <svg aria-hidden="true" focusable="false" width="20" height="20">...</svg>
  <span class="sr-only">Save document</span>
</button>
```

**SVG with its own accessible name:**

```html
<svg role="img" aria-labelledby="icon-title" width="24" height="24">
  <title id="icon-title">Warning: system error</title>
  <!-- paths -->
</svg>
```

## Key rules

- Put `aria-hidden="true"` on SVGs that only decorate visible text.
- Add `focusable="false"` so older IE/Edge builds do not insert extra tab stops.
- When the SVG itself must be named, place `<title>` as the first child and point `aria-labelledby` at a unique id.
- Never rely on icon shape alone for meaning in an icon-only control — expose a text name.
- Prefer one accessible-name strategy per control (`aria-label` **or** visible/sr-only text), not both competing names.
