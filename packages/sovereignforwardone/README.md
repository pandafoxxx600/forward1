# sovereignforwardone package snapshot

This directory contains the monorepo-local snapshot for the `sovereignforwardone` integration.

## Included files

- `contract` — integration contract placeholder/manifest for the package boundary.
- `tobackward1` — bridge entrypoint placeholder for backward-compatible handoff work.

## Upstream source

The upstream project is tracked as a Git submodule at `external/sovereignforwardone-submodule`, configured in the repository root `.gitmodules` file.

This repository records the intended submodule mapping in `.gitmodules`. If the gitlink is not present yet, add it locally with:

```bash
git submodule add https://github.com/pandafoxxx600/sovereignforwardone.git external/sovereignforwardone-submodule
```

After the gitlink exists, initialize or refresh the checkout with:

```bash
git submodule update --init --remote external/sovereignforwardone-submodule
```

If the package snapshot needs to be refreshed, copy or generate the required files from the initialized submodule into this directory and commit the resulting changes.
