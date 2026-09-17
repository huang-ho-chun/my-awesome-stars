# codegraph｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/colbymchenry/codegraph)；查閱日期：2026-09-16。

## 1. 這是什麼？

CodeGraph 是給 Coding Agent 用的程式碼關係索引工具。它先掃描專案，建立符號、呼叫、相依與跨檔關係，讓 Agent 可以問「誰呼叫這個函式」「改這裡會影響哪些地方」。它比較像 Agent 的程式庫地圖和查詢層，不是另一個替你寫程式的 Agent，也不只是畫圖網站。

## 2. 對我有什麼用？

你的測試工具與報告流程可能跨 Shell Script、Python 和多個模組。當 Codex 要修改其中一段時，CodeGraph 可以先幫它找相關檔案與呼叫鏈，降低漏看上游或下游的機會。例如改變結果輸出格式前，先查哪些組裝報告的程式會讀這份輸出。

## 3. 使用情境

- **接手陌生專案**：快速找入口、重要模組及其連結。
- **修改前評估**：查某函式的呼叫者、被呼叫者與可能受影響範圍。
- **與 Agent 協作**：讓 Codex 先用索引定位，再打開實際程式碼確認。

## 4. 我要怎麼用？

1. 按 README 的 [Get Started](https://github.com/colbymchenry/codegraph#get-started) 安裝 CLI；Windows 有 PowerShell 安裝方式，也可用 npm 安裝器。
2. 讓安裝器連接你使用的 Agent。README 說明這一步會設定 Agent，但**不會替專案建立索引**。
3. 到你想分析的專案執行初始化，建立該專案的 graph；之後請 Codex 查一個具體問題，例如某個報告函式的影響範圍。
4. 對照實際檔案、測試和最新修改確認查詢結果。

## 5. 值不值得研究？

**有特定情境時很有用。** 跨多檔、難追相依性的專案值得試；單檔腳本或小修正通常直接搜尋更快。
