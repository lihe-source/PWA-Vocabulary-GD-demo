# V5.7 更新紀錄

更新日期：2026/06/06

## 本次更新

- 將「練習模式」下拉選單共用化，並套用至：
  - 單字拼寫
  - 文章撰寫
  - AI 詢問
- 使用者可在文章撰寫與 AI 詢問頁面直接透過下拉選單切換練習模式。
- 移除統計頁面內「匯出統計資料 CSV」按鈕，避免與設定頁匯出功能重複。
- 統計頁保留練習次數、總答題數、整體正確率摘要。
- 更新設定頁 Gemini AI 模型選單：
  - 移除已不建議使用或已退役的 preview / latest alias 模型。
  - 新增 / 保留目前較適合文字學習功能的 Gemini 3 / Gemini 2.5 模型。
- 更新 AI fallback 順序，優先使用 Gemini 3.5 / 3.1 系列，再以 Gemini 2.5 系列作為備援。
- 版本更新為 `V5_7 / V5.7`，同步更新 `app.js`、`sw.js`、`manifest.json`、`version.json` 與頁面標題。

## V5.7 AI 模型清單

- Gemini 3.5 Flash（推薦）
- Gemini 3.1 Flash-Lite（快速）
- Gemini 3 Flash Preview（Preview）
- Gemini 3.1 Pro Preview（高階）
- Gemini 2.5 Flash（備援）
- Gemini 2.5 Flash-Lite（備援）
- Gemini 2.5 Pro（備援）

## 自我檢查

- `node --check app.js`
- `node --check sw.js`
- `manifest.json` JSON 檢查
- `version.json` JSON 檢查
- ZIP 解壓縮檢查
- 主要檔案存在檢查
