# Wikidata Places

[English](README.md)

Wikidata の座標付き item を Loqi の正規化スキーマへ落としたもの。

## ライセンス

- **CC0-1.0** — CC0 1.0 Universal
- 全文: https://creativecommons.org/publicdomain/zero/1.0/
- 帰属表示: 要らない(出所は manifest に書いてある)
- Share-Alike: 要らない

## 出所

**提供元のライセンスと、このデータセットのライセンスは別。**
対応表が ODbL でも、そこに出てくる Wikidata は CC0 のままである。

- Wikidata — `CC0-1.0`

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

## 分類の付け方

Wikidata の P31 は具体的すぎる(「香取神社」「橋上駅」「廃寺」)ので、
P279* で上位アンカーへ束ねている。束ねる順番は `pipelines/places/lib/schema.mjs` の
`WIKIDATA_KIND_ANCHORS` にあり、**先に見たものが勝つ** — 城・寺社・駅を山や建物より前に置いてある。

どのアンカーにも当たらなかったものは `other`。生の P31 は `source_kinds` に残るので、
後から語彙を足せば拾い直せる。