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

`SOURCE-INPUTS.json` records hashes of original pre-export inputs; expected public-export transformations may make those hashes differ from the final output bytes. `SOURCE-MANIFEST.json` records hashes of the final public files. `SOURCE-PROVENANCE.json` records the product identity, shared-engine digest and both manifest digests. It contains no private repository origin or revision.
