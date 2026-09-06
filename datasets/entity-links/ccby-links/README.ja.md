# Entity links (CC BY side)

[English](README.md)

Wikidata と GeoNames のレコードが同じ場所を指しているという対応表。

## ライセンス

- **CC-BY-4.0** — Creative Commons Attribution 4.0 International
- 全文: https://creativecommons.org/licenses/by/4.0/
- 帰属表示: **要る**
- Share-Alike: 要らない

## 出所

**提供元のライセンスと、このデータセットのライセンスは別。**
対応表が ODbL でも、そこに出てくる Wikidata は CC0 のままである。

- Wikidata — `CC0-1.0`
- GeoNames — `CC-BY-4.0`

## ファイル

| ファイル | 中身 |
| --- | --- |
| `<region>.jsonl` | 1 行 1 レコード。**こちらが正典** |
| `<region>.parquet` | 同じ内容の列指向版(`to_parquet.py` が作る) |
| `manifest.json` | 何から、いつ、どう作ったか。行数とファイルの指紋 |
| `schema.json` | 列の意味 |
| `LICENSE` | 配る側が負う義務 |

## なぜ統合しないのか

出典ごとに条件が違うから。CC0 のつもりで配ったものが実は ODbL だった、は後から直せない —
配った先の誰かが既に取り込んでいる。だから**出典の境界を、そのまま配布の境界にしてある**。

横断して検索したいときは Loqi Places API を使う。あちらは境界を保ったまま、
問い合わせのときだけ束ねて、応答には必ず `sources[]` を添えて返す。

## この対応表のライセンスについて

左(wikidata-places)と右(geonames-places)の両方を見て作った判断なので、
**厳しいほうのライセンスに従う**。「同じ場所だ」という一行は、両方のデータベースから
抽出した情報であって、どちらか片方のものではない。

## 決められないものは書いていない

候補が二つ以上見えたときは一行も書かない。「春日神社」は日本中にあり、
距離で絞っても二つ残ることがある。**間違った対応表は、無い対応表より悪い** —
API が二つの場所を一つに畳んで返し、受け取った側はそれが起きたことに気づけない。

落とした件数は manifest.json の `skipped` にある。