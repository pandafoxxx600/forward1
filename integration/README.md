# sovereignforwardone integration

This integration adds the `sovereignforwardone` upstream project to the JusticeWithinUs monorepo in two forms:

1. A monorepo-local package snapshot under `packages/sovereignforwardone/`.
2. A configured upstream submodule path at `external/sovereignforwardone-submodule`.

## Files added

- `.gitmodules` configures the upstream submodule URL and local path.
- `packages/sovereignforwardone/` contains the local package snapshot boundary files.
- `external/sovereignforwardone-submodule/README.md` documents how to initialize the submodule checkout.
- `integration/pr_body.md` provides a draft pull request body for this integration.

## Local setup

After checking out this branch, inspect whether the submodule gitlink is present:

```bash
git submodule status
```

If the path is not listed, convert the placeholder into a real submodule with:

```bash
git submodule add https://github.com/pandafoxxx600/sovereignforwardone.git external/sovereignforwardone-submodule
git add .gitmodules external/sovereignforwardone-submodule
git commit -m "chore: add sovereignforwardone submodule"
```

## Future follow-up

- Add workspace configuration if this repository adopts pnpm, Yarn, npm, Lerna, or another package/workspace manager.
- Add CI checks for contract validation and package synchronization.
- Add a synchronization script if the package snapshot should be regenerated from the upstream submodule.
