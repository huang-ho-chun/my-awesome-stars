# AutoRAG｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/Marker-Inc-Korea/AutoRAG/blob/HEAD/README.md)；查閱日期：2026-09-16。

## 1. 這是什麼？

目前首頁描述的是 AutoRAG 新版文件「館員」Agent：查找 PDF、Wiki、筆記等，讀原檔並整理編號知識單元；舊版自動尋找最佳 RAG 管線仍放在 `legacy/`。兩者用途不同，不能沿用舊印象。

## 2. 對我有什麼用？

你的私人知識庫若分散在多個本機資料源，它主張在原地檢索並保留來源身份，值得觀察。但它需要配置模型與索引相關組件，生成答案的證據仍要人工檢查。

## 3. 使用情境

在非敏感小資料夾測試一個跨文件問題，查看回答的來源、`evidence` 資料以及錯誤時能否回到原檔。另比較你已在用的本機搜尋流程。

## 4. 我要怎麼用？

先讀 README 的 Configuration 與安裝說明；執行 `autorag init` 產生設定，再以 `autorag refresh` 建立資料來源狀態，使用 `autorag status` 檢查新鮮度，最後 `autorag search` 試問。若想研究舊版 RAG AutoML，應改讀 `legacy/README.md`。

## 5. 值不值得研究？

尤其要注意版本定位：README 說舊版仍維護，但新功能集中在新版。若你的目的是自動比較分塊、檢索器和模型組合，應研究 `legacy/`；若目的是跨資料源查找證據，才試新版館員流程。

**有特定情境才有用。**個人文件檢索可能有價值，但新舊產品定位與依賴需先釐清。
