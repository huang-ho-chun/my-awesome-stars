# ECC 專案指南

來源：[官方 README.md](https://github.com/affaan-m/ECC/blob/HEAD/README.md)｜查閱日期：2026-09-16

## 1. 這是什麼？

ECC 是給多種 Coding Agent 的規則、Skills、hooks、子 Agent 和工作流程集合。現行 README 把它定位為 Agent 工作環境，而非單一「程式品質打分工具」；安裝可以依 profile 與平台選擇。

## 2. 對我有什麼用？

你已使用 Codex 且有自己的工作規範，可借它檢視哪些測試、審查或交接規則值得採納。完整安裝可能與現有指令衝突，應先挑一個能驗證收益的元件。

## 3. 使用情境

以非正式測試專案試一項審查或驗證 Skill，記錄它是否改善 Shell/Python 任務的缺陷發現率、回答長度與工作時間；檢查 hooks 是否改動你預期的操作。

## 4. 我要怎麼用？

README 的 guided setup 提供 `npx ecc-universal@2.2.1 setup` 等例子，但版本應以現行文件為準。先使用 `--target codex --dry-run` 預覽安裝內容，再選 minimal/profile，檢查要寫入的設定與回復方式；勿直接覆蓋既有個人規則。

## 5. 值不值得研究？

導入時需先清點你現有的 AGENTS.md、Skills、hooks 與自訂規則，記錄安裝前狀態。只選一個有明確痛點的元件做一週試驗，觀察 Codex 是否更常遵守驗證與回報要求，再決定是否擴大。

**有特定情境才有用。**可作規範素材庫，但整套導入需要處理與現有 Codex 設定的重疊。
