# Loqi OSM AI Enrichment

[日本語](README.ja.md)

AI-inferred semantic labels derived only from ODbL OpenStreetMap place data.

## License

- **ODbL-1.0** — Open Database License v1.0
- Full text: https://opendatacommons.org/licenses/odbl/1-0/
- Attribution: required
- Share-Alike: required

## Sources

- OpenStreetMap contributors — `ODbL-1.0`
- Loqi — `ODbL-1.0`

## Files

- `index.json`: available regions and their manifests
- `schema.json`: record schema
- `regions/<ISO code>/<region id>/manifest.json`: ordered files, counts, sizes, and hashes
- `data.jsonl` or `data-*.jsonl`: canonical JSON Lines records
- `LICENSE`: redistribution terms for this dataset

Source records stay in separate license-family datasets. Cross-source lookup may link
records at query time, but this directory never silently mixes license families.
