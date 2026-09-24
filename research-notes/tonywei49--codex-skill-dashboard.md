# codex-skill-dashboard｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/tonywei49/codex-skill-dashboard/blob/main/README.md)；查閱日期：2026-09-24。

## 1. 這是什麼？

這是一個在本機執行的 Codex Skills 管理與統計儀表板。它掃描已安裝 Skills、顯示啟用或暫停狀態，透過 SQLite 記錄實際使用事件，並可查看任務標題、專案路徑與時間。它也能翻譯 Skill 描述、複製 Skill 名稱，以及透過更新 Codex 設定來暫停較少使用的 Skill。

它由 Python 標準函式庫、SQLite 和一般 HTML／JavaScript／CSS 組成，不需要額外 Python 套件，也沒有常駐背景服務。

## 2. 對我有什麼用？

你安裝了不少 Skills，這個工具可幫你分辨「已啟用」和「曾實際使用」，找出長期沒用卻仍出現在新對話路由資訊中的 Skills。暫停不常用項目可能讓清單更容易管理，也可查看哪些專案真的用到哪些 Skill。

但統計依賴它加入的 soft hook；過去歷史不會自動完整還原，數字也不是 Codex 官方用量帳單。安裝程式會修改使用者層級的 Skill 目錄、`~/.codex/config.toml` 與 `~/.codex/AGENTS.md`，使用前應先檢查變更並備份相關設定。

## 3. 使用情境

- 查看目前有哪些 Skills 啟用、暫停或可重新啟用。
- 依實際使用次數清理長期不用的 Skills。
- 查看單一 Skill 在哪些任務和專案中被呼叫。
- 將說明翻成繁體中文，方便瀏覽與搜尋。
- 在多台電腦分別保留各自的本機統計。

## 4. 我要怎麼用？

先複製 Repository 並閱讀安裝腳本會修改的檔案，再備份 Codex 設定。README 的一鍵安裝流程以 shell 腳本為主；Windows 若沒有相容 shell，需先確認執行環境。安裝後以本機位址 `127.0.0.1:7065` 啟動儀表板，先只查看清單和統計。

確認 soft hook 記錄正確後，再嘗試暫停一個確定不常用的 Skill，開新對話驗證設定，並保留重新啟用的方法。批次翻譯會呼叫 Codex CLI，可能消耗使用額度，不要在未核對數量前一次全部執行。

## 5. 值不值得研究？

**有特定情境才有用。** 當 Skills 數量多到難以管理時很實用；目前專案規模小、星數少，且會修改 Codex 使用者設定，建議先閱讀腳本並在可還原的情況下試用。
