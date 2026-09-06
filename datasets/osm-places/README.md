# OSM Places

OpenStreetMap の POI を Loqi の正規化スキーマへ落としたもの。ODbL のまま隔離してある。

## ライセンス

- **ODbL-1.0** — Open Database License v1.0
- 全文: https://opendatacommons.org/licenses/odbl/1-0/
- 帰属表示: **要る**
- Share-Alike: **要る** — 取り込んだデータベースを配るなら同じ条件で開くこと

## 出所

**提供元のライセンスと、このデータセットのライセンスは別。**
対応表が ODbL でも、そこに出てくる Wikidata は CC0 のままである。

- OpenStreetMap contributors — `ODbL-1.0`

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

## ODbL であること

**このデータセットを取り込んだデータベースを配るなら、そちらも ODbL で開くことになる。**
それが嫌なら、このデータセットを使わない — `wikidata-places`(CC0)と
`geonames-places`(CC BY)だけで組むという選択がある。Loqi Places が
データセットを分けているのは、その選択を**選べるようにしておくため**。

Loqi Places API では `license=all` を指定したときにだけ、ここのレコードが返る。
既定は `permissive` で、ODbL は入らない。

## 座標について

way と relation は面や線なので、点が無い。geometry の bounding-box center を
座標にしてあるが、**代表点であって、そこに立てるとは限らない**
(公園の重心は茂みの中、川の重心は水の上)。`source_kinds` を見れば、
面として描かれたものかどうかの見当は付く。