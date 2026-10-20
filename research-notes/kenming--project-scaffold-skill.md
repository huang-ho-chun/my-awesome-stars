# Project Scaffold｜GitHub 專案導覽

> 來源：[kenming/project-scaffold-skill](https://github.com/kenming/project-scaffold-skill) 的 [README](https://github.com/kenming/project-scaffold-skill/blob/main/README.md) 與 [繁體中文說明](https://github.com/kenming/project-scaffold-skill/blob/main/README_zh-TW.md)；查閱日期：2026-10-20。

## 1. 這是什麼？

Project Scaffold 是一個協助開發者和 AI Agent **預覽、調整並建立專案規範與文件骨架**的 Agent Skill。你先描述想要的結構，它會顯示附用途註解的目錄樹；調整並確認後，才建立選定的檔案與目錄。

預設骨架包含主規範 `AGENTS.md`、放技術堆疊與驗證原則等細則的 `.agent-rules/`，以及保存需求、研究、架構、開發紀錄、交接與指南的 `docs/`。它提供的是**專案協作與文件的起點**，不會產生應用程式碼、安裝相依套件或替你寫完整 PRD。

## 2. 對我有什麼用？

你常用 Codex 維護不同專案和自動化流程，這個 Skill 可幫你在新專案開始時先決定：規則放哪裡、研究資料如何保存、開發與驗證紀錄放哪裡，以及交接文件如何安排。例如新建一個 GitHub Stars 整理工具時，可以先預覽是否需要 `AGENTS.md`、`docs/research/`、`docs/tracking/`，再把不需要的部分移除。

若既有專案的規範和文件已經清楚，則只需參考它的目錄設計或選擇性補缺，不必為了符合模板重整整個專案。README 說明它遇到不同內容的既有檔案會回報衝突，不會強制覆寫。

## 3. 使用情境

- **新專案初始化**：先建立 Agent 規則、需求、研究與追蹤資料的位置，再開始實作。
- **既有專案補結構**：預覽缺少的文件目錄與規範檔，只加入有明確用途的部分。
- **跨專案一致性**：在多個 CLI 工具、網站或 Agent Skills 專案中沿用相近的文件起點。
- **只想參考模板**：閱讀預設樹與繁體中文 README，手動採用合適部分即可。

## 4. 我要怎麼用？

先看專案的 [繁體中文 README](https://github.com/kenming/project-scaffold-skill/blob/main/README_zh-TW.md) 與預設骨架。正式使用需要可讀取本機 Skill 的 Agent，以及生成時使用的 Node.js 24+。將整個 `skills/project-scaffold/` 資料夾（包含腳本和參考檔）複製到對應 Skills 目錄；Codex 在 Windows 的使用者層級位置是 `%USERPROFILE%\.agents\skills\project-scaffold\`。一般使用不需 `npm install`。

在目標專案中請 Agent「使用 project-scaffold 預覽本專案的骨架，讓我調整結構後再建立」。看到目錄樹後，直接提出新增、刪減、改名或移動要求；核對最終預覽，再確認建立。若只是測試，可要求「只進行模擬，不建立任何檔案」，或指定暫存目標位置。

生成器預設先預覽；相同既有內容會略過，衝突會回報。多檔寫入並非原子操作，部分失敗也不會自動回滾，因此在既有重要專案使用時，先檢查預覽和 Git 變更較穩妥。

## 5. 值不值得研究？

**很適合你在建立新工具或 Agent 專案時試用。** 它把「先討論目錄用途、預覽、確認再建立」變成固定流程，能減少規範和研究資料散落。現有專案已有成熟結構時，先收藏並借用設計即可。
