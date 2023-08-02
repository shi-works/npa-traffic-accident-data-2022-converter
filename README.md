# traffic-accident-data-2022-converter
## プログラムについて
- 本プログラムは、警察庁が公開している、[交通事故統計情報のオープンデータ（2022年）の本票](https://www.npa.go.jp/publications/statistics/koutsuu/opendata/2022/opendata_2022.html)を[コード表](https://www.npa.go.jp/publications/statistics/koutsuu/opendata/2022/opendata_2022.html)を元に読みやすいデータ（GISデータ）に変換するプログラムになります。
- Pythonで構築

### csvfile-to-degree.py
- マージした本票CSVファイル（2019～2021年）の「地点　緯度（北緯）」と「地点　経度（東経）」を十進法度単位に変換するプログラムになります。
- 文字コードをUTF-8に変換します。

#### 使用データ
- `https://xs489works.xsrv.jp/pmtiles-data/traffic-accident/data/honhyo_2022.csv`,62.8MB

#### 出力結果
- `https://xs489works.xsrv.jp/pmtiles-data/traffic-accident/honhyo_2022_to-degree.csv`,73.8MB  

### csvfile-convert.py
- 十進法度単位に変換した本票CSVファイル（2022年）をコード表を元に読みやすいデータに変換するプログラムになります。

#### 使用データ
- `https://xs489works.xsrv.jp/pmtiles-data/traffic-accident/honhyo_2022_to-degree.csv`,73.8MB  
- コード表`https://github.com/shi-works/traffic-accident-data-2022-converter/tree/main/code`

#### 出力結果
##### csv形式
- `https://xs489works.xsrv.jp/pmtiles-data/traffic-accident/honhyo_2022_convert.csv`,221.0MB  
##### FlatGeobuf形式
- `https://xs489works.xsrv.jp/pmtiles-data/traffic-accident/honhyo_2022_convert.fgb`,354.2MB

### 使用データ及び出力結果のライセンスについて
本データセットは[CC-BY-4.0](https://pmtiles-data.s3.ap-northeast-1.amazonaws.com/traffic-accident/LICENSE)で提供されます。使用の際には本レポジトリへのリンクを提示してください。

また、本データセットは交通事故統計情報のオープンデータ（2022年）の本票を加工して作成したものです。本データセットの使用・加工にあたっては、[警察庁Webサイトの利用規約](https://www.npa.go.jp/rules/index.html)を必ずご確認ください。
