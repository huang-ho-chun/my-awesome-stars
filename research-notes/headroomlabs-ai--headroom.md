# headroom 專案指南

來源：[headroomlabs-ai/headroom 官方 README](https://github.com/headroomlabs-ai/headroom/blob/HEAD/README.md)；查閱日期：2026-09-16。

## 1. 這是什麼？

替 Agent 壓縮上下文、包裝 CLI 並共享記憶的工具。

## 2. 對我有什麼用？

README 列 Codex 等宿主和 Python、TypeScript 介面；可處理冗長工具輸出，但其包裝層可能影響執行與認證，應先用無敏感資料試驗。

## 3. 使用情境

選一個長測試日誌任務，記錄原本 token 與找錯結果；接上 Headroom 後重跑，檢查壓縮是否保留真正關鍵的錯誤行和引用位置。

## 4. 我要怎麼用？

README 建議用 uv 安裝 Python CLI，也提供 pip、npm SDK 與 Docker。選代理包裝、MCP 或程式庫模式之一，依文件啟動後用 savings 觀察數據；需要撤回時用 unwrap。

README 的 Python 套件提供 CLI，也有 npm 的 TypeScript SDK；Agent wrap、MCP 與內嵌函式屬不同整合層。先選一種模式，避免把多個壓縮路徑疊在一起而難以比對。

## 5. 值不值得研究？

有特定情境才有用：大量日誌或多 Agent 上下文開銷明顯時才值得增加中介層。
