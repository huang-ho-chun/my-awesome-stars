# Ix｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/ix-infrastructure/Ix/blob/main/README.md)；查閱日期：2026-09-28。

## 1. 這是什麼？

Ix 是為程式庫建立持久系統圖的程式碼理解工具。它解析符號、呼叫、匯入與關係，讓人或 Coding Agent 以結構化查詢了解元件、執行流程和修改影響。
圖譜保存在本機，支援 27 種程式語言及多種設定與資料格式；可透過 CLI 和 MCP 連接 Codex、Claude Code、Cursor、Gemini 等工具。

## 2. 對我有什麼用？

你可以在接手陌生專案、進行跨檔案修改或準備重構時，先用 Ix 建立架構地圖，再讓 Codex 查詢特定服務、流程或影響範圍。它可減少每次對話重新讀大量檔案，也能在不同工作階段保留結構索引。
它主要回答靜態程式結構；商業規則、執行期資料與真實行為仍要配合文件、測試和實際執行驗證。

## 3. 使用情境

- 新專案導覽：查詢某個類別或服務的用途與相依關係。
- 修改前評估：追蹤函式呼叫與可能受影響的元件。
- Coding Agent 上下文：透過 MCP 提供較小、較相關的結構片段。
- 多語言程式庫：同時索引 TypeScript、Python、Go、Rust、PowerShell 等內容。

## 4. 我要怎麼用？

1. 依官方安裝方式安裝 `ix`；README 首頁目前提供 macOS／Linux 安裝指令，Windows 使用前要先查官方 Windows 支援或改在 WSL 試用。
2. 在目標專案執行 `ix map .` 建立圖譜。
3. 先用 `ix explain`、`ix trace` 和 `ix impact` 驗證它是否正確理解關鍵模組。
4. 需要 Agent 整合時，先用 `ix mcp install --dry-run` 預覽，再執行安裝；Codex 也可手動註冊 `ix mcp`。

## 5. 值不值得研究？

**值得在較大的程式庫試用。** 它和你使用 Codex 理解專案的流程直接相關。Windows 原生安裝路徑需要先確認，因此可先在 WSL 或非關鍵專案做小型驗證，再考慮長期使用。
