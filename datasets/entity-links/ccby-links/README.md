# Entity links (CC BY side)

[日本語](README.ja.md)

Conservative links between Wikidata and GeoNames records that describe the same place.

## License

- **CC-BY-4.0** — Creative Commons Attribution 4.0 International
- Full text: https://creativecommons.org/licenses/by/4.0/
- Attribution: required
- Share-Alike: not required

## Sources

- Wikidata — `CC0-1.0`
- GeoNames — `CC-BY-4.0`

## Files

- `index.json`: available regions and their manifests
- `schema.json`: record schema
- `regions/<ISO code>/<region id>/manifest.json`: ordered files, counts, sizes, and hashes
- `data.jsonl` or `data-*.jsonl`: canonical JSON Lines records
- `LICENSE`: redistribution terms for this dataset

Source records stay in separate license-family datasets. Cross-source lookup may link
records at query time, but this directory never silently mixes license families.
