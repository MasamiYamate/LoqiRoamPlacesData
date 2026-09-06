# Entity links (CC BY side)

[日本語](README.ja.md)

Conservative links between Wikidata and GeoNames records that describe the same place.

## License

- **CC-BY-4.0** — Creative Commons Attribution 4.0 International
- Full text: https://creativecommons.org/licenses/by/4.0/
- Attribution: required
- Share-Alike: not required

## Sources

- [Wikidata](https://www.wikidata.org/) — `CC0-1.0`
- [GeoNames](https://www.geonames.org/) — `CC-BY-4.0`

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

Loqi-authored prose is [CC0-1.0](../../../DOCUMENTATION-LICENSE.md). Dataset files remain under their dataset license.
