# ruflo 專案指南

來源：[ruvnet/ruflo 官方 README](https://github.com/ruvnet/ruflo/blob/HEAD/README.md)；查閱日期：2026-09-16。

## 1. 這是什麼？

供 Claude Code 和 Codex 使用的多 Agent 編排框架。

## 2. 對我有什麼用？

README 涵蓋 swarm、記憶、工作流、工具與擴充；能力範圍大，較適合需要多角色分工的複雜任務。你目前的 Shell/Python 測試工作未必需要整套框架。

## 3. 使用情境

選一個可切分的非客戶專案，例如資料擷取、報告格式、品質驗證三部分，試其分工與整合；比較人工審查負擔是否下降。

## 4. 我要怎麼用？

依 README 可先用 npx ruflo init wizard 做互動設定，或選對應 Codex／Claude Code plugin。從最小配置開始，建立任務後檢查角色權限、記憶內容與產出差異，避免直接套進正式流程。

README 的 Quick Start 分為 Claude Code 精簡 plugin 路徑與 CLI 初始化精靈；Codex 相關整合另有套件。先辨明目前宿主支援的功能，再評估 swarm 與記憶是否有必要。

## 5. 值不值得研究？

可以先收藏，以後可能用到：多 Agent 協調有潛力，但初期設定與審核成本高。
