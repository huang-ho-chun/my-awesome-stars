# Modern Web Guidance｜GitHub 專案導覽

> 專案：https://github.com/GoogleChrome/modern-web-guidance

## 1. 這是什麼？

Modern Web Guidance 是提供給 Coding Agent 的現代網頁開發指引與命令列工具。README 說明它涵蓋瀏覽器 API、CSS 佈局、效能、表單、無障礙及相容性等主題；Agent 可依任務搜尋並取回特定指南，而不是把整套材料放進對話。專案另提供 Chrome 擴充功能開發的 Skill 套件。

## 2. 對我有什麼用？

開發網頁時，可用它查找較新的平台能力與實作範例，協助 Coding Agent 避免沿用過時做法。對需要兼顧跨瀏覽器、無障礙與效能的介面工作，指南可作為查詢及審查的起點，最後仍須在目標瀏覽器實測。

## 3. 使用情境

- 請 Coding Agent 製作對話框、彈出介面或動畫時，查相關原生 API、限制及替代方案。
- 對既有網站掃描舊式寫法，再評估是否值得改用現代平台功能。
- 在採用新 CSS 或瀏覽器 API 前，檢查相容性、漸進增強與可存取性考量。
- 開發 Chrome 擴充功能時，選用 README 列出的專用 Skill 套件。

## 4. 我要怎麼用？

1. 先在專案 README 查看 Quickstart 與支援的 Agent 安裝方式。若使用 Node.js／npm，可執行 `npx modern-web-guidance@latest install`，依互動式精靈選擇整合方式。
2. 想先試內容而不安裝 Skill，可用 `npx modern-web-guidance@latest search "問題描述"` 搜尋，再用 `retrieve "指南 ID"` 取回指南；`legacy-scan .` 可掃描目前程式庫的舊式模式。
3. 把指南用於實際任務後，檢查產出的程式碼與目標瀏覽器。README 說明實驗性 Origin Trial 和波動較大的新功能預設受控，需要在 `.mwgrc` 明確啟用。

CLI 的指南搜尋與讀取可在本機離線運作；README 也說明工具預設收集匿名使用資訊，包括安裝次數、指南 ID 與 CLI 搜尋字詞，可用 `DISABLE_TELEMETRY=1` 關閉。以 `npx` 首次執行或更新仍涉及取得 npm 套件。

## 5. 值不值得研究？

如果常讓 Coding Agent 寫前端，值得先挑一個正在處理的介面問題比較指南與既有做法，特別是相容性及無障礙細節。指南有助於提出更好的候選方案，但不會取代專案自己的瀏覽器測試與設計判斷。
