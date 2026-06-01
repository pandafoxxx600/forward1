# sovereignforwardone submodule placeholder

This directory is reserved for the `sovereignforwardone` upstream repository configured in `.gitmodules`:

```text
https://github.com/pandafoxxx600/sovereignforwardone.git
```

This placeholder is not the upstream checkout itself. If the path is not yet a gitlink, replace this placeholder by adding the submodule locally:

```bash
git submodule add https://github.com/pandafoxxx600/sovereignforwardone.git external/sovereignforwardone-submodule
```

After the gitlink exists, initialize or refresh the checkout with:

```bash
git submodule update --init --remote external/sovereignforwardone-submodule
```

The remote repository content is intentionally not vendored here; it should be populated by Git submodule initialization.
