# geo_graph
## 必要なもの
- geojsonファイル（ex. osaka_jinko.geojson）
  - 今回は国土地理院のデータを利用、参考文献参照
- mapboxのapiAccessToken

## ローカルで動かす場合
- サーバー（例えばlive-server）
https://qiita.com/cigalecigales/items/33afaa42f91542ffa62e
- ネット環境（地図データを引いてくるため）

## 参考文献
https://qiita.com/t-mat/items/b896cff2222ef7f416a5

### 上記参考文献で修正したところ
```
const getlatlon=(feature) =>{
    let geo = feature.geometry.coordinates[0];
```
の最後の部分に[0]を追加し以下にする
```
const getlatlon=(feature) =>{
    let geo = feature.geometry.coordinates[0][0];
```

