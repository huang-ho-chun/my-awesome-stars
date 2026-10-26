# Graphify｜GitHub 專案導覽

> 來源：[Graphify-Labs/graphify](https://github.com/Graphify-Labs/graphify) README；查閱日期：2026-10-26。

## 1. 這是什麼？

Graphify 是將程式庫及相關文件轉成可查詢知識圖的 CLI 與 Agent Skill。它本機解析程式碼中的呼叫、匯入、繼承等關係，整理跨檔案連結、子系統與重要節點，提供查詢、追路徑和解釋功能。README 說基本程式碼解析不需 LLM 或向量資料庫；文件與多媒體的語意處理則可能需要另行設定後端。

## 2. 對我有什麼用？

當你面對不熟悉的程式庫，想知道某個功能從哪裡進入、依賴哪些檔案、改動可能碰到什麼地方，可以先建圖再問 Agent。它對中大型、文件多的專案尤其有用；對只有幾個檔案的小工具，直接搜尋可能更快。你已收藏其他程式碼關係工具，Graphify 可作為另一個實際比較候選，重點看索引耗時、關係是否準確、查詢是否節省閱讀時間。

## 3. 使用情境

- 新接手程式庫時，找核心模組與呼叫路徑。
- 修改功能前，查跨檔案依賴與相關 ADR／文件。
- 讓 Codex 等 Agent 先參考本機圖譜，再回答架構問題。

## 4. 我要怎麼用？

README 要求 Python 3.10+，建議先用 uv 安裝官方 PyPI 套件 `graphifyy`（雙 y），CLI 名稱仍是 `graphify`。接著執行 `graphify install --platform codex` 安裝 Skill，於目標專案讓 Codex 使用 `$graphify`；也可用 `graphify install --project --platform codex` 只安裝到目前專案。先對一個可公開測試的 repo 建圖、跑幾個你知道答案的查詢，檢查結果和磁碟成本。PDF、Office、MCP 等能力需選配 extras；只有在需要時再裝。不要把 Graphify Cloud 的宣傳能力誤認為本機版預設功能。

## 5. 值不值得研究？

**很適合你研究程式庫時試用。** 先在一個熟悉專案驗證關係圖是否可靠，再決定要不要加入日常 Codex 流程。
