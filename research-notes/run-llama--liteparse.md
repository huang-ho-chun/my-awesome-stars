# LiteParse｜GitHub 專案導覽

> 依 [專案 README](https://github.com/run-llama/liteparse) 與相關文件於 2026-09-16 重寫；著重用途與使用判斷，不深入原始碼。

## 1. 這是什麼？

LiteParse 是把 PDF 與其他文件轉成程式和 AI 較容易使用之資料的輕量解析工具。它可產出文字、Markdown 或結構化 JSON，也能處理 OCR、表格、版面與文字位置等資訊。它比較像文件處理管線的**前處理工具**，不是會自己回答文件問題的聊天 App。

## 2. 對我有什麼用？

你有技術 PDF、報告和各類工作文件需要整理。LiteParse 可以先把原件轉成結構化資料，再交給你的 Markdown 報告流程或 AI 分析。例如一份含測試表格的 PDF，先轉成 Markdown，確認數值和表格順序，再拿來做重點摘要或比對。它也適合未來建立 RAG 或 Wiki 的文件入口。

## 3. 使用情境

- **單份文件整理**：PDF 轉 Markdown，供閱讀、編修或 Agent 使用。
- **批次前處理**：多份文件先統一格式，再交給後續程式。
- **需要回指原件的流程**：用 JSON 中的版面或位置資訊，協助追溯文字在原 PDF 的位置。

## 4. 我要怎麼用？

1. 依 README 的 [Installation](https://github.com/run-llama/liteparse#installation) 選擇環境：有 Node.js／TypeScript、Python、Rust 套件，亦有瀏覽器 WASM；多數安裝方式提供 `lit` CLI。你若只是先試解析，可選熟悉的 Python 或 CLI 路線。
2. 先挑一份有標題、表格與圖片的代表性 PDF，輸出 Markdown；需要頁面位置時再試 JSON。
3. 對照原 PDF 檢查閱讀順序、表格欄位、數字、OCR 結果與圖片位置。結果可靠後，才把它接進自動化流程。

## 5. 值不值得研究？

**很適合你試用。** 你的文件整理與 AI 工作流需要穩定的前處理；但對掃描件、多欄與複雜表格，仍須保留原件並人工抽查。
