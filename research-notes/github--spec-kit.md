# spec-kit｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/github/spec-kit/blob/HEAD/README.md)；查閱日期：2026-09-16。

## 1. 這是什麼？

GitHub 的規格導向開發工具組，替 Coding Agent 提供範本、流程和可留下的決策紀錄。README 將新功能規格、修 Bug 和想法評估列為三個獨立入口；後兩者是另外安裝的擴充。

## 2. 對我有什麼用？

你有跨人協作的測試系統與客戶設定，需求容易散在對話裡。Spec Kit 可讓一次較大的變更先寫清楚需求、限制、驗收方法與驗證紀錄，減少 Agent 自行猜測。

## 3. 使用情境

在下一個涉及多檔案的報告功能或測試框架調整上，先做精簡規格，讓 Codex 根據規格規劃、實作，再逐條核對驗收。若只改一行設定，不必套整套流程。

## 4. 我要怎麼用？

依 README 備妥 Python、`uv` 與支援的 Agent；用 `uv tool install specify-cli` 安裝，然後 `specify init` 建專案並指定對應 Agent integration。既有程式庫請優先讀 README 連結的 existing-project 指南，避免初始化覆蓋既有文件。

## 5. 值不值得研究？

你可先把最小成功標準寫成三條：需求可被非作者理解、驗收條件可執行、實作後能回查改動理由。若規格文件反而重複既有 Issue 而沒有減少誤解，應精簡模板，不必為維持流程而維持流程。

**有特定情境才有用。**適合需求不明或跨多人工作；日常小修不需增加流程負擔。
