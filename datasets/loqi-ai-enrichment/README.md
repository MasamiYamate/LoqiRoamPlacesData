# Loqi AI Enrichment

[日本語](README.ja.md)

AI-inferred semantic labels derived only from CC0 place data. They are suggestions, not observations.

## License

- **CC0-1.0** — CC0 1.0 Universal
- Full text: https://creativecommons.org/publicdomain/zero/1.0/
- Attribution: not required
- Share-Alike: not required

## Sources

- Wikidata — `CC0-1.0`
- Loqi — `CC0-1.0`

## Files

- `index.json`: available regions and their manifests
- `schema.json`: record schema
- `regions/<ISO code>/<region id>/manifest.json`: ordered files, counts, sizes, and hashes
- `data.jsonl` or `data-*.jsonl`: canonical JSON Lines records
- `LICENSE`: redistribution terms for this dataset

Source records stay in separate license-family datasets. Cross-source lookup may link
records at query time, but this directory never silently mixes license families.
