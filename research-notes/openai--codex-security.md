# Codex Security｜GitHub 專案導覽

> 專案：https://github.com/openai/codex-security

## 1. 這是什麼？

Codex Security 提供程式庫安全檢查的 Codex 工作流程、命令列工具與 TypeScript SDK。README 列出掃描整個 repository、指定路徑或 Git 差異，驗證候選弱點、產生修補建議、檢查既有修補，以及匯出報告等用途。掃描完成會保存報告與發現，供後續閱讀與核對。

## 2. 對我有什麼用？

在修改驗證、授權或其他敏感程式後，可用它先找可能的漏洞，再根據報告中的原始碼證據與排除範圍判斷是否要修。也可掃描既有專案，將結果整理成可追蹤的安全工作。掃描結果是待驗證的發現，不應直接視為已確認漏洞。

## 3. 使用情境

- 針對登入與權限控制程式執行指定範圍掃描。
- 比對 `origin/main` 以檢查本次變更可能引入的安全問題。
- 讀取已保存的報告，要求驗證發現或檢查修補是否有效。
- 需要自動化時，以 SDK 或 GitHub Action 執行定期掃描並匯出結果。

## 4. 我要怎麼用？

若已在 Codex 啟用 Codex Security plugin，可依 README 的 [Agent 工作流程](https://github.com/openai/codex-security/blob/main/docs/agent-workflows.md)要求掃描，並閱讀保存的報告、來源證據及涵蓋限制。若使用 CLI，README 要求 Node.js 22.13.0 以上的 22.x，或 Node.js 24／26，以及 Python 3.10 以上；安裝 `@openai/codex-security`、完成 `cs login` 後，在專案目錄執行 `cs scan .`。可用 `--path` 或 `--diff origin/main` 縮小範圍。先核對授權、成本與資料傳送設定，再掃描含私人程式碼的 repository。

## 5. 值不值得研究？

若維護需要安全檢查的程式庫，值得用一個可控範圍試跑，評估報告的證據、誤報與實際修復價值。它適合輔助調查與驗證，正式修補仍需人工審查、測試與部署流程。
