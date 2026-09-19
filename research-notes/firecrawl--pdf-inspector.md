# pdf-inspector｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/firecrawl/pdf-inspector/blob/main/README.md)；查閱日期：2026-09-20。

## 1. 這是什麼？

pdf-inspector 是 Firecrawl 開發的 Rust PDF 處理 Library，也提供 Python、Node.js、瀏覽器 WebAssembly 與命令列工具。它會先快速判斷 PDF 是文字型、掃描型、圖片型或混合型，再擷取可用文字並轉成 Markdown。擷取時會考慮文字座標、欄位閱讀順序、標題、清單、程式碼、表格、粗斜體與頁面分隔等結構。

它的核心價值是先做**文件分類與路由**：一般文字 PDF 直接在本機解析，只有需要的頁面才交給 OCR。這可減少所有 PDF 都走 OCR 所需的時間與資源。它是供開發者整合的底層工具，不是打開就能整理文件的圖形介面。

## 2. 對我有什麼用？

你會處理 PDF、掃描文件與需要保留來源的筆記。pdf-inspector 適合放在自動化流程的前段，先判斷每頁能否直接抽取文字，再決定哪些頁面需要 OCR 或人工檢查。例如：

- 批次整理 PDF 前，先將文字型文件轉成 Markdown，把掃描件送往 OCR。
- 對混合型 PDF 只辨識必要頁面，避免整份文件都做較慢的 OCR。
- 擷取研究報告、發票、法律文件或多欄論文，盡量保留閱讀順序與表格結構。
- 將輸出的 Markdown 接到 Obsidian、RAG 索引或後續 AI 摘要流程。

如果只是偶爾手動閱讀一份 PDF，MinerU、現成 OCR 軟體或可直接上傳文件的 Agent 會比較省事。pdf-inspector 的優勢在於你要建立可重複、可程式化的本機處理流程。

## 3. 使用情境

### 一般文字 PDF

快速抽取文字並轉成乾淨 Markdown，適合報告、論文、發票與合約等以文字為主的文件。

### 掃描與混合文件

先取得整份與逐頁分類結果，將確實需要辨識的頁面送往選擇性 OCR；遇到字型編碼問題時也能標示應改走 OCR。

### 批次資料管線

用 JSON 或 Library API 接到後續程式，根據文件類型、信心分數與頁面結果決定解析、OCR、人工複核或託管服務的路徑。

### 本機或瀏覽器處理

Rust、Python、Node.js 可用於本機或伺服器流程；WebAssembly 版本可在瀏覽器或 Web Worker 本機解析，不必把每份文件傳到伺服器。

## 4. 我要怎麼用？

最容易的入門方式取決於你現在的流程：

- **Python：** 安裝 `pdf-inspector`，呼叫 `process_pdf()`，取得 PDF 類型和 Markdown。
- **Node.js：** 安裝 `@firecrawl/pdf-inspector`，讀入 PDF 位元組後呼叫 `processPdf()`。
- **命令列：** 安裝 Rust CLI 後，用 `pdf2md document.pdf` 轉換，或用 `detect-pdf document.pdf --json` 只做分類。
- **瀏覽器：** 使用 WebAssembly 套件，讓使用者的瀏覽器本機解析 PDF。

建議你先選一份熟悉的文字型 PDF、一份掃描 PDF和一份混合文件做小型測試，比對分類、閱讀順序、表格與頁面標記。基本擷取不需要 OCR；選擇性 OCR 則需要另外準備 PDFium、ONNX Runtime 和模型檔，安裝與部署會更複雜。正式採用前也要用自己的中文文件、特殊字型和掃描品質測試，不能只依賴專案提供的基準測試。

## 5. 值不值得研究？

**有特定情境才有用。** 若你要建立本機 PDF 批次處理、OCR 分流或 RAG 文件匯入流程，它的分類速度、多欄閱讀順序與結構化 Markdown 很值得試；若需求只是偶爾把單一 PDF 轉成筆記，使用較完整的現成工具會更直接。
