## Summary

- Adds a `packages/sovereignforwardone/` package snapshot boundary with integration contract and handoff files.
- Adds `.gitmodules` configuration for the upstream `sovereignforwardone` repository.
- Adds submodule initialization guidance under `external/sovereignforwardone-submodule/`.
- Adds integration documentation for setup and follow-up work.

## Notes

The upstream repository mapping is configured in `.gitmodules` for `external/sovereignforwardone-submodule`. If the gitlink is not present yet, consumers should add it locally with:

```bash
git submodule add https://github.com/pandafoxxx600/sovereignforwardone.git external/sovereignforwardone-submodule
```

After the gitlink exists, initialize or refresh it with:

```bash
git submodule update --init --remote external/sovereignforwardone-submodule
```

## Testing

- Verified the repository status and staged integration files.
- Verified the configured `.gitmodules` file is parseable with `git config --file .gitmodules --get-regexp '^submodule\.'`.
- Checked `git submodule status`; no gitlink is present in this local snapshot because the upstream fetch could not be performed here.
