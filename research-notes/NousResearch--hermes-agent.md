# Hermes Agent｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/NousResearch/hermes-agent/blob/HEAD/README.md)；查閱日期：2026-09-16。

## 1. 這是什麼？

可在終端與訊息平台使用的開源個人 Agent。整合工具調用、持續記憶、技能與排程；README 區分終端互動與 gateway 接入 Telegram、Discord 等訊息管道，並提供原生 Windows 安裝。

## 2. 對我有什麼用？

若你有長期追蹤任務、跨訊息平台互動或本地工具串接需求，可以拿來比較常駐 Agent 的工作方式。它會引入新的設定和資料保存範圍，先用獨立測試環境較容易評估。

## 3. 使用情境

可以用來探索長期運作的助理如何記住工作背景、觸發排程及連接工具；你已有 Codex 工作流，先用獨立測試環境比較能力與維運負擔。

例如在隔離資料夾讓它追蹤公開測試專案的待辦與摘要，觀察記憶何時更新、工具權限如何控制；不要先讓它接觸客戶伺服器憑證。

## 4. 我要怎麼用？

依 README 在 Windows 使用官方 PowerShell 安裝器，或在 WSL2 走 Linux 路徑；安裝後執行 hermes setup 設定模型提供者，先從終端 UI 試一個可驗證任務，再評估 gateway。檢查安裝器將變更的依賴與路徑。

README 區分直接開啟 hermes 終端介面與啟動 gateway 接收訊息；Windows 安裝器還會處理 Python、uv、Node.js 等依賴。最小試用只需完成 setup 後在終端執行一個可檢查的任務。

## 5. 值不值得研究？

有特定情境才有用：若需要常駐或跨訊息管道 Agent 再深入研究；單次開發任務目前可沿用 Codex。
