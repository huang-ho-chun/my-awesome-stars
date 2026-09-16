# commentflow 專案指南

來源：[官方 README.md](https://github.com/sysprog21/commentflow/blob/HEAD/README.md)｜查閱日期：2026-09-16

## 1. 這是什麼？

commentflow 專門重排程式碼中的自然語言註解，支援 C、C++、Rust、POSIX shell 和 GAS 組語。README 說只改註解文字的換行、不改程式碼位元組，且會保留格式化指令、表格、圖示和其他特殊區塊。

## 2. 對我有什麼用？

你有 Shell 自動化腳本，若註解長短凌亂，可在格式化前用它統一欄寬。Python 註解不在 README 支援清單，因此對你的 Python 程式不能直接套用。

## 3. 使用情境

在一支已版本控管的 POSIX shell 腳本上先執行唯讀 diff，檢查 ShellCheck 指令、例子和對齊的表格未被改壞；再決定是否寫回。

## 4. 我要怎麼用？

從 README 的 Prebuilt Binaries 取得合適版本，先用 `commentflow --diff src/foo.c` 或 `--dry-run` 看差異；`--check` 可供 CI 檢測，確認後才對目標檔執行寫入。它是註解重排，仍需另外跑 shfmt 與原有測試。

## 5. 值不值得研究？

採用前最好用 `--diff` 人工檢查幾種註解：ShellCheck 標記、範例命令、ASCII 圖、對齊表格。README 說工具對不確定區域偏保守，所以有些段落可能保持原狀；這是需要知道的邊界，而非一定是故障。

**有特定情境才有用。**適合大量 POSIX shell 註解整理，但不支援你同樣常用的 Python。
