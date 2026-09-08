# Sources — Svelte / SvelteKit

Last checked: 2026-09-08

## Core docs

- Svelte documentation: https://svelte.dev/docs/svelte
- Svelte 5 runes overview: https://svelte.dev/docs/svelte/$state
- `$derived`: https://svelte.dev/docs/svelte/$derived
- `$effect`: https://svelte.dev/docs/svelte/$effect
- `$props` / `$bindable`: https://svelte.dev/docs/svelte/$props
- SvelteKit documentation: https://svelte.dev/docs/kit
- SvelteKit load functions: https://svelte.dev/docs/kit/load
- SvelteKit form actions: https://svelte.dev/docs/kit/form-actions
- SvelteKit hooks: https://svelte.dev/docs/kit/hooks
- SvelteKit adapters: https://svelte.dev/docs/kit/adapters
- Migration guide (Svelte 4 → 5): https://svelte.dev/docs/svelte/v5-migration-guide
- Svelte error codes / compiler warnings: https://svelte.dev/docs/svelte/compiler-warnings

## Testing and tooling

- Vitest: https://vitest.dev/
- Playwright: https://playwright.dev/
- svelte-check: https://github.com/sveltejs/language-tools/tree/master/packages/svelte-check

## Refactor verification notes

- Prefer `$derived` over `$effect` + assignment for pure computations.
- Keep browser-only APIs behind `onMount` / `$effect` / `browser` checks for SSR safety.
- Prefer form actions with progressive enhancement over client-only mutation paths.
