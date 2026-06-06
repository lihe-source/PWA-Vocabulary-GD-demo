# V5.6 更新紀錄

更新日期：2026-06-06

## 修正
- 統一 App 顯示版本為 `V5_6 / V5.6`。
- 修正設定頁「清除全部單字」使用錯誤 localStorage key 的問題，現在會正確清除 `vocabWords` 並同步清除單字加權設定。
- 修正 Service Worker 在不支援的瀏覽器或 WebView 中可能造成初始化錯誤的問題。
- 更新檢查改以 `version.json` 為主，不再解析 `sw.js`，降低版本判斷失敗機率。

## 優化
- Service Worker 新增 `version.json` 快取，並只攔截同網域靜態資源；Google 登入、Google Drive、Gemini API、CDN 與字型不再被快取攔截。
- CSV 匯入改用可支援引號與換行欄位的解析流程，降低文章、AI 回覆、例句匯入錯誤。
- AI 詢問、AI 單字查詢、AI 批改、例句顯示與 ECDICT 查詢結果加入 HTML escape，降低使用者輸入或 AI 回覆造成畫面異常的風險。
- Google Drive 合併備份時，單字比對改為大小寫不敏感，並相容 `english` / `wordEn` 欄位。
- Gemini 模型清單更新至 2026-06-06 可見的 API 模型，加入 Gemini 3 Flash Preview、Gemini 3.1 Pro Preview、Gemini 3.1 Flash-Lite Preview。
- iOS PWA 介面增加水平溢出保護，降低 chips、AI 回覆、長文字造成左右滑動的機率。

## 檔案架構
- 維持原本 `PWA-Vocabulary-GD-main/` 根目錄與主要檔案位置，方便直接覆蓋原 GitHub Pages 專案測試。
