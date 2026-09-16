# AI Job Search（MadsLorentzen/ai-job-search）

資料來源：[官方 README](https://github.com/MadsLorentzen/ai-job-search/blob/HEAD/README.md)；查閱日期：2026-09-16。

## 1. 這是什麼？

以 Claude Code 為基礎的求職工作流程倉庫。README 說明使用者 fork 後填寫個人資料，再以指令搜尋職缺、評估適配度、客製履歷與求職信、準備面試；資料主要在本機處理。它依賴 Claude Code 的命令與資料夾結構，不能直接把相同指令視為 Codex 原生功能。

## 2. 對我有什麼用？

你將外商與可轉移技能視為未來選項，但目前沒有立即換工作的明確需求。這套框架可先參考「把經歷寫成有情境和成果的證據」的方式，整理 Shell／Python、自動化測試與客戶設定案例；若真正開始求職，再評估是否採用完整流程。履歷中的職責、數字與職缺解讀仍應人工查證。

## 3. 使用情境

例如日後看到一個測試工程或 FDE 職缺，可先用自己確認過的工作經歷寫三則 STAR 案例，對照職缺所需技能，而非讓 AI 補出沒有做過的專案。若使用自動草稿，要逐句確認日期、工具、職級、成果及個資；任何外部提交由你最後決定。

## 4. 我要怎麼用？

README 的 Quick start 是 fork 並 clone 倉庫，準備 Python 3.10 以上與 Claude Code，安裝其中的求職工具，填寫個人 profile，再在 Claude Code 使用 `/scrape`、`/apply`、`/interview` 等工作指令。`pypdf` 可選裝以檢查 PDF 可解析性。先用一則職缺完成搜尋與草稿流程，檢查產出，再考慮實際投遞。

## 5. 值不值得研究？

有特定情境才有用：真正啟動求職時可省整理時間；現在先保存可核實的職涯素材，比導入整套工具更合適。
