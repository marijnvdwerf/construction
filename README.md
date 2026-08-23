# Construction fonts

Construction is a typeface family containing Construction Sans (Light, Bold, and Mini) and Construction Serif (Regular), built from the UFO sources in `src/`.

## Build locally

With [uv](https://docs.astral.sh/uv/) installed:

```sh
uv sync
uv run fontmake -u src/*.ufo -o otf --output-dir build/otf --validate-ufo
uv run fontmake -u src/*.ufo -o ttf --output-dir build/ttf --validate-ufo
```

The generated OpenType fonts are written to `build/otf/` and the TrueType fonts to `build/ttf/`.

## Releases

Every push to a version-shaped `v*` tag builds the fonts and publishes `construction-fonts-<tag>.zip` as a GitHub Release. Pushes to `main` and pull requests run the build and upload the fonts as a workflow artifact.

[![Build fonts](https://github.com/marijnvdwerf/construction/actions/workflows/build.yml/badge.svg)](https://github.com/marijnvdwerf/construction/actions/workflows/build.yml)
