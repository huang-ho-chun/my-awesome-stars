# SkillOpt｜GitHub 專案導覽

> 依 [專案 README](https://github.com/microsoft/SkillOpt) 與相關文件於 2026-09-16 重寫；著重用途與使用判斷，不深入原始碼。

## 1. 這是什麼？

SkillOpt 是改善 AI Agent Skill 的工具與研究框架。它把寫給 Agent 的 Skill 文件當成可優化的對象：讓 Agent 執行一組任務，根據結果提出文字修改，再以保留的驗證任務決定要不要採用。它不是訓練新的語言模型，也不是一般聊天工具；適合已經在維護 Skills、而且能判斷修改是否帶來改善的人。專案另有 **SkillOpt-Sleep**，從日常 Agent 工作紀錄找重複問題，產生待審核的改善提案。

## 2. 對我有什麼用？

你已經使用 Codex、調整 Skills 與 `AGENTS.md`。若某個 Skill 經常在同類任務失敗，你可以用它建立「做任務 → 找失敗 → 修改指引 → 驗證」的循環。例如讓一個報告產生 Skill 處理幾份不同輸入，觀察是否漏步驟，再比較修訂前後的結果。對你來說，先研究 SkillOpt-Sleep 從既有工作紀錄提取問題，比直接架完整訓練實驗更貼近日常。

## 3. 使用情境

- **日常使用者**：回顧 Codex session，找出反覆需要你糾正的地方，整理成 Skill 改進候選。
- **Skill 維護者**：準備一組代表性任務和評分標準，測試某段指引是否真的提升品質。
- **研究者**：比較不同 Agent、任務與驗證策略；這一層需要較多實驗準備，暫時不必先做。

## 4. 我要怎麼用？

1. 先挑一個你常用且有明確失敗案例的 Skill，保存原版與幾個測試任務。
2. 依 [SkillOpt-Sleep 文件](https://github.com/microsoft/SkillOpt/blob/main/docs/sleep/README.md)了解紀錄擷取、回放、驗證和人工採用的流程；README 指向 `skillopt-sleep` CLI，基本套件可用 Python 套件方式安裝。
3. 先在副本或小範圍任務試跑，檢查它提出了什麼修改、驗證有沒有涵蓋你重視的失敗。
4. 只有你核對結果後才把新 Skill 用到日常工作。完整 SkillOpt 訓練流程可等你有穩定評分方式再研究。

## 5. 值不值得研究？

**很適合你研究，但先小規模試用 SkillOpt-Sleep。** 它與你持續改進 Codex 工作方式的需求吻合；完整優化框架需要任務集與驗證標準，成本比一般安裝 Skill 高。
