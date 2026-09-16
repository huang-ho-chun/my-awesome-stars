# open-code-review 專案指南

來源：[官方 README.md](https://github.com/alibaba/open-code-review/blob/HEAD/README.md)｜查閱日期：2026-09-16

## 1. 這是什麼？

OpenCodeReview 是偏向本機程式碼審查的 CLI 與 Agent 整合工具。README 強調先以確定性規則選檔和解析，再讓 LLM 對差異做判斷；可看工作目錄、分支差異、單次提交或整份檔案。

## 2. 對我有什麼用？

你做 Shell/Python 自動化與伺服器設定變更時，可在交付前用它多看一輪漏掉的邊界條件、危險操作與維護性問題。建議把結果當審查線索，仍由人核對程式與測試輸出。

## 3. 使用情境

挑一個有明確需求與測試的變更，在提交前檢查未提交差異；再與人工審查比較誤報與遺漏。可特別觀察它是否理解設定檔、Shell 引號與報告輸出的契約。

## 4. 我要怎麼用？

README 提供 `npm install -g @alibaba-group/open-code-review`；安裝後在測試儲存庫依 CLI 範例檢查 workspace、branch range 或 commit，也可將結果存檔供 Codex 讀取。先看 prerequisite 與模型設定，避免把含機密的差異送到不合適的服務。

## 5. 值不值得研究？

試用結果應分成可重現缺陷、合理但不急迫建議、誤報三類，並以原始 diff 和測試結果核對。若工具需要雲端模型，先確定程式碼與客戶設定的資料邊界；單次審查的文字評語不能代替正式測試。

**有特定情境才有用。**程式變更多、需第二輪審查時有益；小改動仍以實際測試為主。
