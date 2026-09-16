# SkillSpector 專案指南

來源：[NVIDIA/SkillSpector 官方 README](https://github.com/NVIDIA/SkillSpector/blob/HEAD/README.md)；查閱日期：2026-09-16。

## 1. 這是什麼？

掃描 Agent Skills 安全風險的 Python 工具。

## 2. 對我有什麼用？

會檢查技能檔、命令與可疑模式，適合你安裝第三方 Codex Skill 前做初篩；掃描結果是線索，不能保證安全。

## 3. 使用情境

對一個準備安裝的 Skill 先掃目錄或 Git repo，對每項警示人工閱讀 SKILL.md、腳本與下載行為，再決定是否放入你的主要工作環境。

## 4. 我要怎麼用？

README 提供 uv tool 安裝與 Docker 用法，Python 需符合文件要求。先用 CLI 對本機 Skill 目錄掃描，可選不同輸出格式或不使用 LLM 的模式；審閱報告後再試安裝，不要把無警示視為信任證明。

README 可掃本機 Skill 目錄、單一 SKILL.md、Git repo 或 zip，且有不使用 LLM 的掃描模式。對準備安裝的第三方技能，先掃來源目錄最容易把警示對應到實際檔案。

## 5. 值不值得研究？

很適合我，可以實際使用：你常處理第三方 Agent Skills，安裝前掃描是具體而低成本的輔助。
