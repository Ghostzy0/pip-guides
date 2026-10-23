# Pip Guides edition map

This custom product publishes exactly the three editions listed in `distribution.json`. The local default is `pip` (Pip Core).

| Variant | Product name | Features | Default |
| --- | --- | --- | --- |
| `baseline-enhanced` | Neutral Plus | Neutral presentation with Find steps |  |
| `pip` | Pip Core | Pip presentation without Find steps | Default |
| `pip-enhanced` | Pip Plus | Pip presentation with Find steps |  |

## Build

```sh
./scripts/build-app.sh
./scripts/build-app.sh baseline-enhanced
./scripts/build-app.sh pip-enhanced
```

Find steps and Command-F are present only in Plus variants. All editions share local storage, capture, image editing and export behavior; each bundle uses a separate app/data identity. See [public verification](../PUBLIC-VERIFICATION.md) for current evidence and limitations.

`SOURCE-PROVENANCE.json` records the product identity, shared-engine digest, exact source-input manifest hashes and the public-file manifest hash. It contains no private repository origin or revision.
