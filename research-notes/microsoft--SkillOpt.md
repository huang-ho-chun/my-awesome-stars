# SkillOpt｜研究說明

> 依先前對話重整的研究筆記，非逐字稿。專案功能可能隨版本改變。

**專案**：[microsoft/SkillOpt](https://github.com/microsoft/SkillOpt)

## 你當時問的重點

你提供 `microsoft/SkillOpt`，想知道它是什麼，以及對你使用 Codex、撰寫與改進 Skills 有沒有實際價值。

## 先前說明

SkillOpt 優化的是給既有 LLM Agent 使用的自然語言 Skill，不是修改模型權重。它讓 Agent 跑任務，收集成功與失敗案例，提出 Skill 文字修改，再用驗證任務比較效果；有效才保留。研究時也談到 SkillOpt-Sleep：從日常 Agent 工作紀錄擷取重複問題，作為改善 Skill 的線索。

## 對你的用處與用法

你已在調整 Codex Skills、`AGENTS.md` 和工作規範。可先挑一個常用、且有明確失敗案例的 Skill，記錄目前結果，再研究 SkillOpt-Sleep 如何從既有 session 找問題；確定能衡量改善後，再試完整優化流程。

## 使用前要核對

先界定成功標準與驗證任務，避免只因文字看起來更好就接受修改。
