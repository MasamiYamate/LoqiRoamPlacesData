# GeoNames Places

[English](README.md)

GeoNames の地名データを Loqi の正規化スキーマへ落としたもの。

## ライセンス

- **CC-BY-4.0** — Creative Commons Attribution 4.0 International
- 全文: https://creativecommons.org/licenses/by/4.0/
- 帰属表示: **要る**
- Share-Alike: 要らない

## 出所

**提供元のライセンスと、このデータセットのライセンスは別。**
対応表が ODbL でも、そこに出てくる Wikidata は CC0 のままである。

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

## 帰属表示

このデータセットを配るときは **GeoNames への帰属表示が要る**。
manifest.json の `attribution` をそのまま添えればよい。

## 分類の付け方

GeoNames の feature code は最初から粗いので、平たい対応表で足りる
(`GEONAMES_KIND_BY_FEATURE`)。当たらなかったものは `other` で、
生の `<class>.<code>` は `source_kinds` に残る。

## 文書ライセンス

Loqi作成の本文は[CC0-1.0](../../DOCUMENTATION-LICENSE.md)です。データには各データセットのライセンスが適用されます。
