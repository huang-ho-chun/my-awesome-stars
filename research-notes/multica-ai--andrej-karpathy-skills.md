# andrej-karpathy-skills 專案指南

來源：[multica-ai/andrej-karpathy-skills 官方 README](https://github.com/multica-ai/andrej-karpathy-skills/blob/HEAD/README.md)；查閱日期：2026-09-16。

## 1. 這是什麼？

根據 Karpathy 對 Coding Agent 常見錯誤的觀察整理的工作指引。

## 2. 對我有什麼用？

四個重點是先釐清、維持簡單、局部修改及以可驗證目標執行。這些規則與你重視保存原始內容和驗證結果的做法一致。

## 3. 使用情境

挑一個需要小幅修改的 Shell/Python 腳本，要求 Agent 先指出假設、改動範圍與驗證方式；比較是否少做了無關重構。

## 4. 我要怎麼用？

README 以 Claude Code plugin 安裝為主，也有其他編輯器用法。若在 Codex 使用，先閱讀 CLAUDE.md 的原則並轉成相容的專案指示或 Skill，按你的現有規範調整，再用實際任務測試。

README 將原則分為 Think Before Coding、Simplicity First、Surgical Changes、Goal-Driven Execution。用既有腳本的小修正試驗這四點，比直接加入大量新規範更能看出差異。

## 5. 值不值得研究？

很適合我，可以實際使用：原則本身可直接用於現有 Codex 流程，無須導入複雜服務。
