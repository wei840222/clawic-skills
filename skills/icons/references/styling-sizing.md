# Color Inheritance

```html
<svg fill="currentColor" aria-hidden="true" focusable="false" width="20" height="20">
  <path d="..."/>
</svg>
```

`currentColor` inherits from the CSS `color` property, so hover and theme changes recolor the icon automatically:

```css
.button { color: blue; }
.button:hover { color: red; } /* icon turns red too */
```

Remove hardcoded `fill="#000"` (or equivalent) before relying on `currentColor`.

For stroke-based icons, set `stroke="currentColor"` and usually `fill="none"`.

# Sizing

Standard grid sizes: 16, 20, 24, 32px.

Match stroke weight to size:

| Size | Stroke | Use case |
|------|--------|----------|
| 16px | 1px | Dense layouts, small text |
| 20px | 1.25px | Default compact UI |
| 24px | 1.5px | Buttons, primary actions |
| 32px | 2px | Headers, navigation |

Touch targets need at least 44×44 CSS pixels. The glyph may be smaller when padding expands the hit area:

```css
.icon-button {
  box-sizing: content-box;
  width: 24px;
  height: 24px;
  padding: 10px; /* 24 + 20 = 44px touch target */
}
```

# Scaling with Text

```css
.icon {
  width: 1em;
  height: 1em;
}
```

The icon then scales with surrounding text size. Keep the parent `color` intentional so `currentColor` icons stay legible.
