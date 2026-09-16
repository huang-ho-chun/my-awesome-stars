# codex-keysmith 專案指南

來源：[Jia-Ethan/codex-keysmith 官方 README](https://github.com/Jia-Ethan/codex-keysmith/blob/HEAD/README.md)；查閱日期：2026-09-16。

## 1. 這是什麼？

用帶版本的腳本管理 Codex 指令與 hooks 部署。

## 2. 對我有什麼用？

對你持續使用 Codex Skills 和自訂規範的情況，可提供狀態檢查、預覽與回復機制；但它會動到 Codex 設定，需先理解每項寫入。

## 3. 使用情境

在測試用 Codex 目錄比較現有規範與預計部署的變更，確認是否會與你的個人 Skills、既有 hooks 和專案說明衝突，再試回復流程。

## 4. 我要怎麼用？

依 README 從 Releases 取得穩定版腳本；先執行 --version、--status 和 --dry-run，檢查目標目錄、來源與寫入計畫。確認後才用 --yes 部署，需要移除時用 restore-hooks 或 uninstall 流程。

README 的流程刻意分成 status、dry-run、yes 和 uninstall／restore-hooks。試用時保存 dry-run 輸出並與原設定比對，才看得出它將覆蓋或新增哪些 Codex 檔案。

## 5. 值不值得研究？

有特定情境才有用：當你要在多部機器或多份環境維持相同 Codex 設定時才值得導入。
