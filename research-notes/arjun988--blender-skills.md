# Blender Skills｜GitHub 專案導覽

> 專案：https://github.com/arjun988/blender-skills

## 1. 這是什麼？

這是為 Blender 工作流程整理的 Agent Skills 集合。README 列出建模、材質、燈光、場景、最佳化與輸出等專業技能，並以 `blender-director` 將需求導向不同技能。它支援 Cursor、Claude Code、Kiro 與 Codex；要讓 Agent 實際操作 Blender，還需連接 Blender MCP。

## 2. 對我有什麼用？

製作 3D 資產時，可讓 Agent 按較完整的工作步驟處理需求，例如先建立模型，再處理 UV、材質、燈光與匯出。技能文件可作為指引；實際成果仍要在 Blender 檢視拓樸、比例、材質與輸出格式。

## 3. 使用情境

- 依參考圖製作硬表面道具，並檢查比例與材質。
- 建立場景或角色後，安排 UV、燈光、渲染與引擎匯出。
- 讓 Agent 按任務路由適合的技能，而非每一步重新描述流程。

## 4. 我要怎麼用？

先讀 README、[Skills Guide](https://github.com/arjun988/blender-skills/blob/main/SKILLS_GUIDE.md) 與 [Blender MCP 設定](https://github.com/arjun988/blender-skills/blob/main/docs/BLENDER_MCP_SETUP.md)。依所用 Agent 安裝技能資料夾；若需要直接修改場景，安裝 uv 與 Blender MCP addon，確認 Blender 與 MCP 用戶端已連通。從小型物件試做，逐步檢查場景並保留可回復版本。

## 5. 值不值得研究？

若已用 Blender 且希望 Agent 協助重複的 3D 步驟，值得挑一條短流程試用。其價值取決於 MCP 連線穩定度、技能品質與人工驗收；沒有 Blender MCP 時，這些技能不能直接替你操作場景。
