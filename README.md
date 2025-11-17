# polygon-tool

這是一個純前端的小工具，讓使用者上傳 CSV（需包含 `VillageCode` 欄位），並根據事先準備好的 VillageCode → Polygon WKT 對照表，產生固定模板格式的 GeoJSON。

## Demo
https://huilingkao.github.io/polygon-tool/

## 功能介紹
- 上傳含 `VillageCode` 欄位的 CSV。
- 讀取 `village_polygons.json` 中對應欄位的 WKT 資料。
- 轉換為固定模板的 GeoJSON，並可下載結果。

## 專案結構
- `index.html`：主要的網頁程式與 UI。
- `village_polygons.json`：VillageCode→WKT 對照資料（需定期更新）。

## 使用方式
1. 點擊「Choose File」選擇 CSV 檔（表頭需包含 `VillageCode`）。
2. 按下「轉換成 GeoJSON」按鈕。
3. 轉換成功後，可複製結果或按「下載 GeoJSON」。

## 注意事項
- CSV 的欄位名稱應為 `VillageCode`、`Village_Code` 等已支援的變形。
- `village_polygons.json` 必須包含對應 VillageCode 的 WKT。
- 如果要更新 WKT 對照表，記得重新匯出並覆蓋 `village_polygons.json`。

## 開發與部署
1. 修改 `index.html` 或 `village_polygons.json` 後，記得 commit + push 到 `main`。
2. GitHub Pages 已設定使用 `main` 分支的根目錄，推送後會自動部署。

## License
© 2025 HuiLingKao
