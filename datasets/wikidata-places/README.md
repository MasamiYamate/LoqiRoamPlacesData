# Wikidata Places

[日本語](README.ja.md)

Coordinate-bearing Wikidata items normalized to the Loqi Places schema.

## License

- **CC0-1.0** — CC0 1.0 Universal
- Full text: https://creativecommons.org/publicdomain/zero/1.0/
- Attribution: not required
- Share-Alike: not required

## Sources

- [Wikidata](https://www.wikidata.org/) — `CC0-1.0`

## Changes from source

Loqi selected records and normalized field names, classifications, and output structure.
This is an adapted dataset, not an unchanged source dump.

## Files

- `index.json`: available regions and their manifests
- `schema.json`: record schema
- `regions/<ISO code>/<region id>/manifest.json`: ordered files, counts, sizes, and hashes
- `data.jsonl` or `data-*.jsonl`: canonical JSON Lines records
- `LICENSE`: dataset license notice and canonical legal-text URI

Source records stay in separate license-family datasets. Cross-source lookup may link
records at query time, but this directory never silently mixes license families.

## Documentation license

Loqi-authored prose is [CC0-1.0](../../DOCUMENTATION-LICENSE.md). Dataset files remain under their dataset license.
