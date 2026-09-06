# Loqi AI Enrichment

[English](README.md)

CC0 の場所データだけを材料に、AI が意味情報(タグ・雰囲気・活動・向き)を生成したもの。

## ライセンス

- **CC0-1.0** — CC0 1.0 Universal
- 全文: https://creativecommons.org/publicdomain/zero/1.0/
- 帰属表示: 要らない(出所は manifest に書いてある)
- Share-Alike: 要らない

## 出所

**提供元のライセンスと、このデータセットのライセンスは別。**
対応表が ODbL でも、そこに出てくる Wikidata は CC0 のままである。

- Wikidata — `CC0-1.0`
- Loqi — `CC0-1.0`

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

## AI推測ラベル

各行は名前・分類・地域からAIが推測したラベルで、現地観測や事実認定ではない。
`model`、`prompt_version`、`generated_at`、`input_hash`を使って生成条件を追跡できる。
JSONLは一定件数ごとの不変パートとして追加され、manifestの順序で読む。