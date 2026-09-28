# Graft｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/trailhq/Graft/blob/main/README.md)；查閱日期：2026-09-28。

## 1. 這是什麼？

Graft 是為 Coding Agent 建立本機程式碼上下文圖的 CLI。它把程式庫整理成可重建的圖檔，讓 Claude Code、Cursor、Codex、Gemini 等 Agent 取得與目前任務相關的節點，而不必反覆把整個檔案塞入上下文。
它提供搜尋、地圖、呼叫者、影響範圍與視覺化命令，也可作為 MCP server。產生的 `graft/` 是本機快取，預設不提交到 Git。

## 2. 對我有什麼用？

你可以用它加速大型或陌生程式庫的導覽，讓 Codex 在修改前取得較精準的結構背景。這和 Ix、GitNexus、codegraph 類似，值得以同一個專案比較建立索引時間、查詢品質和對實際修改的幫助。
README 的效能與成本數據來自專案自己的基準；是否能在你的程式庫重現，仍要自行量測。

## 3. 使用情境

- 大型程式庫導覽：用地圖和搜尋快速定位功能與相依模組。
- 修改影響評估：查詢呼叫者或 blast radius，補助人工審查。
- Agent 自動帶入上下文：依提示內容取回相關圖節點。
- 多倉庫或 monorepo：建立跨資料夾的結構索引與視覺圖。

## 4. 我要怎麼用？

1. 安裝 Node.js 後，以 `npm install -g @nanonets/graft` 安裝，或用 `npx` 直接試跑。
2. 在非關鍵專案先執行 `graft init --dry-run` 查看它會修改哪些檔案，再執行 `graft init` 選擇要連接的 Agent。
3. 用 `graft map`、`graft grep`、`graft callers` 等命令檢查索引是否有用；產生的圖是可重建快取。
4. Codex 等工具可透過 MCP 使用；若程式庫更新，工具會依設定刷新圖譜。正式導入前應檢查寫入的 Agent 設定與 `.gitignore` 變更。

## 5. 值不值得研究？

**值得和現有程式碼圖工具做實測比較。** 它的安裝與 Agent 整合路徑簡單，對大型 codebase 可能有直接效益。先用一個熟悉的專案驗證查詢正確性與實際節省的上下文，再決定保留 Graft、Ix 或其他方案。
