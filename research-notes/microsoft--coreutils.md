# Coreutils for Windows

> 專案：[microsoft/coreutils](https://github.com/microsoft/coreutils)｜依據：專案 README（2026-10-29 查閱）

## 1. 這是什麼？

這是 Microsoft 維護的 Windows 版 Unix 常用命令套件，打包 uutils/coreutils、findutils 與 grep 等工具。目的在 Windows 原生命令列提供熟悉的命令與參數；README 標示目前仍是 Preview。

## 2. 對我有什麼用？

你在 Windows PowerShell 工作，又會接觸 Linux 或客戶伺服器；安裝後可試著在兩邊使用相近的 `grep`、`sort` 等命令與腳本。但同名 PowerShell 指令、別名與 PATH 順序可能改變實際執行的程式，既有自動化需逐一驗證。

## 3. 使用情境

適合跨 Windows/Linux 操作、搬移 shell 腳本或在 Windows 直接試 Unix 指令。若你的腳本已穩定使用 PowerShell 原生指令，沒有必要為一致性全面改寫。

## 4. 我要怎麼用？

先閱讀 README 的 Shell conflicts 與 Windows caveats，再用 `winget install Microsoft.Coreutils` 或 Releases 安裝。於 PowerShell 7.4 以上先測少數不衝突命令，透過 `--help` 查參數；遇到同名指令時明確指定可執行檔或調整呼叫方式，確認管線行為後才放進正式腳本。

## 5. 值不值得研究？

很適合你收藏與試用，尤其常在 Windows 與 Linux 間切換；Preview 階段應先在非正式腳本驗證相容性。
