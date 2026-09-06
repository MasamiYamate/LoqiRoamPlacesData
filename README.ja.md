# LoqiRoam Places Data

[English](README.md)

Loqiが正規化した公開POIデータを、出典とライセンス族ごとに分離して配布するリポジトリです。

出典レコードは統合せず、`entity-links/`に同一場所と保守的に判断できた対応だけを置きます。
AI推測ラベルは独立した`loqi-*-ai-enrichment`データセットに収録し、現地観測や確定事実では
ないこと、モデル、プロンプト版、入力hash等の来歴を各行に残します。

## ダウンロード

最初に[`index.json`](index.json)を読んでください。各データセットは独自の`index.json`を持ち、
`regions/<ISO国コード>/<region id>/`以下に成果物を置きます。JSONLが正典で、大きなファイルは
レコード境界で`data-*.jsonl`へ分割され、manifestの順番で読みます。

## ライセンス

このリポジトリには複数の独立したライセンスが含まれます。**全体へ一つのライセンスが適用される
わけではありません。** 各データセット直下の`LICENSE`と[`LICENSING.ja.md`](LICENSING.ja.md)を
確認してください。
