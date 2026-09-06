# Entity links (ODbL side)

[日本語](README.ja.md)

Conservative links between Wikidata and OpenStreetMap records, isolated under ODbL.

## License

- **ODbL-1.0** — Open Database License v1.0
- Full text: https://opendatacommons.org/licenses/odbl/1-0/
- Attribution: required
- Share-Alike: required

## Sources

- Wikidata — `CC0-1.0`
- OpenStreetMap contributors — `ODbL-1.0`

## Files

- `index.json`: available regions and their manifests
- `schema.json`: record schema
- `regions/<ISO code>/<region id>/manifest.json`: ordered files, counts, sizes, and hashes
- `data.jsonl` or `data-*.jsonl`: canonical JSON Lines records
- `LICENSE`: redistribution terms for this dataset

Source records stay in separate license-family datasets. Cross-source lookup may link
records at query time, but this directory never silently mixes license families.
