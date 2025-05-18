# jica.pmtiles 🇯🇵🗺️

OpenStreetMap から抽出した JICA Offices の地理データを PMTiles 形式で公開しています！

## 🚀 データへのアクセス

- PMTiles データはこちらからダウンロードできます：
  👉 [jica.pmtiles](https://hfu.github.io/jica.pmtiles/jica.pmtiles)

## 👀 PMTiles Viewer で見る

- [PMTiles Viewer で開く](https://pmtiles.io/?url=https://hfu.github.io/jica.pmtiles/jica.pmtiles)

---

## 📜 ライセンス
このデータは OpenStreetMap から抽出されており、[Open Database License (ODbL)](https://opendatacommons.org/licenses/odbl/) のもとで提供されています。

## 技術的原理

このリポジトリの Makefile には、`pmtiles` タスクが定義されています。

- Overpass API を使って OpenStreetMap から JICA Offices のデータ（ノード・ウェイ・リレーション）を取得します。
- 取得したデータは `jq` で GeoJSONSeq 形式に変換されます。
- その GeoJSONSeq を `tippecanoe` にパイプし、PMTiles 形式（jica.pmtiles）に変換・出力します。

この一連の処理により、最新の JICA Offices データを簡単に PMTiles 形式で生成できます。

## その他

jica.pmtiles は Quick Mapping Project の一部です。

このリポジトリは Generative AI の支援で作成されています 🤖✨

ご意見・ご要望は [UNopenGIS/qmp Issue #1](https://github.com/UNopenGIS/qmp/issues/1) までどうぞ！
