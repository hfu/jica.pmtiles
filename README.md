# jica.pmtiles 🇯🇵🗺️

OpenStreetMap から抽出した JICA Offices の地理データを PMTiles 形式で公開しています！

JICA Offices geodata extracted from OpenStreetMap, published as PMTiles!

## 🚀 データへのアクセス / Access the Data

- PMTiles データはこちらからダウンロードできます：
  👉 [jica.pmtiles](https://hfu.github.io/jica.pmtiles/jica.pmtiles)
- Download the PMTiles data here:
  👉 [jica.pmtiles](https://hfu.github.io/jica.pmtiles/jica.pmtiles)

## 👀 PMTiles Viewer で見る / View in PMTiles Viewer

- [PMTiles Viewer で開く / Open in PMTiles Viewer](https://pmtiles.io/?url=https://hfu.github.io/jica.pmtiles/jica.pmtiles)

---

## 📜 ライセンス / License
このデータは OpenStreetMap から抽出されており、[Open Database License (ODbL)](https://opendatacommons.org/licenses/odbl/) のもとで提供されています。

This data is extracted from OpenStreetMap and provided under the [Open Database License (ODbL)](https://opendatacommons.org/licenses/odbl/).

## 技術的原理 / Technical Overview

このリポジトリの Makefile には、`pmtiles` タスクが定義されています。

- Overpass API を使って OpenStreetMap から JICA Offices のデータ（ノード・ウェイ・リレーション）を取得します。
- 取得したデータは `jq` で GeoJSONSeq 形式に変換されます。
- その GeoJSONSeq を `tippecanoe` にパイプし、PMTiles 形式（jica.pmtiles）に変換・出力します。

The Makefile defines a `pmtiles` task:
- Fetches JICA Offices data (nodes, ways, relations) from OpenStreetMap using Overpass API
- Converts the data to GeoJSONSeq format with `jq`
- Pipes the GeoJSONSeq to `tippecanoe` to generate the PMTiles file (jica.pmtiles)

この一連の処理により、最新の JICA Offices データを簡単に PMTiles 形式で生成できます。

This process allows you to easily generate up-to-date JICA Offices data in PMTiles format.

## その他 / Other

jica.pmtiles は Quick Mapping Project の一部です。

jica.pmtiles is part of the Quick Mapping Project.

このリポジトリは Generative AI の支援で作成されています 🤖✨

This repository is created with the help of Generative AI 🤖✨

ご意見・ご要望は [UNopenGIS/qmp Issue #1](https://github.com/UNopenGIS/qmp/issues/1) までどうぞ！

For feedback or requests, please visit [UNopenGIS/qmp Issue #1](https://github.com/UNopenGIS/qmp/issues/1).
