# Claude-Code-Game-Studios｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/Donchitos/Claude-Code-Game-Studios/blob/main/README.md)；查閱日期：2026-09-24。

## 1. 這是什麼？

這是一個以 Claude Code 為核心的遊戲開發專案範本，把遊戲工作拆成導演、部門主管與專業角色，包含 49 個 Agents、74 個工作流程 Skills、hooks、路徑規則和文件範本。它支援 Godot 4、Unity 和 Unreal Engine 5，涵蓋企劃、程式、美術、音效、敘事、QA、製作與發行。

它不是會自動替你做完整遊戲的成品生成器，而是**用 Claude Code 組織遊戲專案與人機協作流程的工作室範本**。

## 2. 對我有什麼用？

若你想用 AI 做遊戲，它可提供從概念、引擎設定、故事拆分、開發、測試到發行的現成流程，也會要求視覺變更實際啟動遊戲並保留截圖，避免只看測試通過就當作完成。

它對目前以 Codex 和一般自動化為主的工作關聯較低，而且專案明確以 Claude Code 的指令、hooks 與設定格式設計。大量角色與流程也可能增加上下文、時間和文件量；README 自己的比較顯示較重流程增加可追溯性，卻未必讓遊戲更好玩。

## 3. 使用情境

- 從零建立 Godot、Unity 或 Unreal 遊戲專案。
- 為多人或長期遊戲開發建立 GDD、ADR、Story、QA 和發行規範。
- 讓不同專業 Agent 分工處理玩法、UI、音效、敘事與測試。
- 接手既有遊戲，先判斷階段、補文件並安排下一個可交付項目。
- 用 hooks 檢查提交、資產命名、設定和測試證據。

## 4. 我要怎麼用？

需要 Git 與 Claude Code；jq 和 Python 可增加驗證能力。最簡單的方式是將 Repository 當成新遊戲範本，開啟 Claude Code 後執行 `/start`，再選擇引擎與流程嚴謹度。

第一次建議使用預設的 `minimal`，做一個很小、能執行的原型，確認 AI 真的產生遊戲、啟動檢查並保存視覺證據。等專案規模和團隊需求明確後，再提高到 standard 或 full。若主要使用 Codex，需要自行移植 Claude Code 特有的 hooks 與 Skills，不能假設可直接相容。

## 5. 值不值得研究？

**對我目前用途不大。** 除非你準備使用 Claude Code 開發 Godot、Unity 或 Unreal 遊戲，否則它的角色、流程與文件成本偏高；可以先收藏，真正開始遊戲專案時再研究。
