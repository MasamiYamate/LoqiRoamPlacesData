# OSM Places

[日本語](README.ja.md)

OpenStreetMap POIs normalized to the Loqi Places schema and kept in an ODbL-only dataset.

## License

- **ODbL-1.0** — Open Database License v1.0
- Full text: https://opendatacommons.org/licenses/odbl/1-0/
- Attribution: required
- Share-Alike: required

## Sources

- [OpenStreetMap contributors](https://www.openstreetmap.org/copyright) — `ODbL-1.0`

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
