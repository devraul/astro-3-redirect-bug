# Vercel + Astro 3 + redirect bug

## Repro

1. run `pnpm install`;
2. run `pnpm -F website run build`
3. see the error:
   ```
   11:58:12 [build] Building server entrypoints...
   [vite:load-fallback] Could not load @astro-page:/uses (imported by @astro-page-split:/uses): The argument 'path' must be a string or Uint8Array without null bytes. Received '\x00@astro-page:/uses'
   error   Could not load @astro-page:/uses (imported by @astro-page-split:/uses): The argument 'path' must be a string or Uint8Array without null bytes. Received '\x00@astro-page:/uses'
   TypeError [PLUGIN_ERROR]: Could not load @astro-page:/uses (imported by @astro-page-split:/uses): The argument 'path' must be a string or Uint8Array without null bytes. Received '\x00@astro-page:/uses'
    at TypeError.get (https://githubvnkvuj-ebm4.w-credentialless.staticblitz.com/blitz.33975f1d.js:67:7048)
    at eval (/home/projects/github-vnkvuj/node_modules/.pnpm/astro@3.0.3/node_modules/astro/dist/core/errors/dev/utils.js:35:11)
    at Module.collectErrorMetadata (/home/projects/github-vnkvuj/node_modules/.pnpm/astro@3.0.3/node_modules/astro/dist/core/errors/dev/utils.js:34:7)
    at throwAndExit (/home/projects/github-vnkvuj/node_modules/.pnpm/astro@3.0.3/node_modules/astro/dist/cli/throw-and-exit.js:31:55)
    at cli (/home/projects/github-vnkvuj/node_modules/.pnpm/astro@3.0.3/node_modules/astro/dist/cli/index.js:164:11)
   /home/projects/github-vnkvuj/apps/website:
    ERR_PNPM_RECURSIVE_RUN_FIRST_FAIL  website@0.0.1 build: `astro build`
   Exit status 1
   ```
