# Vercel + Astro 3 + redirect bug

## Repro

1. run `pnpm install`;
2. run `pnpm -F website run build`
3. see the error:
   ```
   [vite:load-fallback] Could not load @astro-page:/uses (imported by @astro-page-split:/uses): The argument 'path' must be a string or Uint8Array without null bytes. Received '\x00@astro-page:/uses'
   error   Could not load @astro-page:/uses (imported by @astro-page-split:/uses): The argument 'path' must be a string or Uint8Array without null bytes. Received '\x00@astro-page:/uses'
   ```
