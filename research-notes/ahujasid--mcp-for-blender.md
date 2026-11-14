# MCP for Blender｜GitHub 專案導覽

> 專案：https://github.com/ahujasid/mcp-for-blender

## 1. 這是什麼？

MCP for Blender 是連接 Blender 與 AI 助理的社群整合工具，非 Blender Foundation 官方專案。它由 Blender addon 和 MCP server 組成，讓支援 MCP 的客戶端依指令讀取或修改 3D 場景。README 指出套件已由 `blender-mcp` 改名為 `mcp-for-blender`，新安裝應使用新名稱。

## 2. 對我有什麼用？

可讓 Coding Agent 協助建立物件、調整材質與場景，並在 Blender 中檢查結果。對需要反覆試不同構圖或快速製作簡單資產的工作，能減少手動操作，但場景品質與操作範圍仍需自行審核。

## 3. 使用情境

- 用自然語言建立簡單 3D 物件或場景草稿。
- 讓 Agent 修改既有場景的物件與材質，再由人檢查結果。
- 與專門的 Blender Agent Skills 搭配，串接較完整的製作流程。

## 4. 我要怎麼用？

閱讀 README 的 Quickstart 與手動設定。Windows 可先安裝 `uv`，再執行 README 所述的 `uvx mcp-for-blender setup` 來設定客戶端與 addon；亦可按手動步驟分別加入 MCP server 和 Blender addon。重新啟動 Agent 應用程式、開啟 Blender，從小場景測試連線。執行任何安裝腳本前，先檢查來源與其將修改的設定；對重要 `.blend` 檔先另存副本。

## 5. 值不值得研究？

若已經在用 Blender 與 MCP 客戶端，值得先做一個可回復的場景實驗。重點是連線是否穩定、工具操作是否可預期，以及能否在 Blender 內驗證每次變更。
