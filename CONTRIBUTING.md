# Contributing to weather-iconic

Thanks for your interest in improving **weather-iconic**! This guide covers how
to set up the project, make changes, and open a pull request.

## Prerequisites

- Node.js `>= 16` (see the `engines` field in `package.json`)
- npm

## Getting started

```bash
git clone https://github.com/konradmichalik/weather-iconic.git
cd weather-iconic
npm ci
```

## Development workflow

```bash
npm run dev        # start the Vite dev server / landing preview
npm run build      # full build: icons, types, bundle, sprite, fonts, png
npm test           # run the test suite (vitest)
npm run typecheck  # type-check with tsc (no emit)
```

The build is split into individual steps you can run in isolation:

| Script | Output |
| --- | --- |
| `npm run build:icons`  | processed SVG icons |
| `npm run build:types`  | TypeScript declarations + icon constants |
| `npm run build:vite`   | the JS/ESM bundle |
| `npm run build:sprite` | the SVG sprite |
| `npm run build:fonts`  | the webfonts (WOFF2, WOFF, TTF) |
| `npm run build:png`    | PNG exports |

## Adding or changing icons

1. Add or edit the source SVG(s) under `src/icons/`.
2. Update `src/icons/metadata.json` so the icon is picked up by the build
   (name, codepoint, categories, etc.).
3. Run `npm run build` and verify the icon appears in the sprite, font, and
   PNG output.
4. Run `npm test` and `npm run typecheck`.

Please keep icons consistent with the existing set — same grid, stroke, and
multi-color conventions.

## Pull requests

- Branch off `main` and keep each PR focused on a single change.
- Make sure `npm test` and `npm run typecheck` pass locally.
- `dist/` is generated output that is committed to the repo (it feeds the
  GitHub Pages landing page and the published package). If your change affects
  the generated output, run `npm run build` so `dist/` stays in sync.
- Use clear, descriptive commit messages.

## Reporting bugs & requesting features

Open an issue describing the problem or idea. For security issues, please
follow the process in [`SECURITY.md`](./SECURITY.md) instead of opening a
public issue.

## License

By contributing, you agree that your contributions will be licensed under the
project's [CC-BY-SA-3.0](./LICENSE) license.
