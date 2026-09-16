# markitdown 專案指南

來源：[官方 README](https://github.com/microsoft/markitdown/blob/HEAD/README.md)｜查閱日期：2026-09-16

## 1. 這是什麼？

輕量 Python 文件轉 Markdown 工具，支援 PDF、Office、HTML、圖片、音訊及部分壓縮與網頁來源。README 說輸出主要供 LLM 或文字分析使用，會保留標題、清單、表格等結構，但不是高保真排版轉換器。

## 2. 對我有什麼用？

你可把它放進 Python 報告與資料前處理管線，將不同檔案轉成較一致的文字格式，再交給搜尋或摘要工具。對掃描件、手寫或複雜版面仍需用專門解析和人工核對。

## 3. 使用情境

選幾份既有 DOCX、PPTX、PDF 和 HTML，轉檔後檢查表格、標題、連結與數字是否完整；特別標出不適合直接入庫的失真案例。

## 4. 我要怎麼用？

依 README 使用 Python 3.10 以上的虛擬環境，安裝 `markitdown[all]` 或只選所需格式 extras；在 CLI 執行 `markitdown path-to-file.pdf -o document.md`。要放進程式可改用 Python API，處理不可信輸入時注意 README 的 I/O 權限提醒。

## 5. 值不值得研究？

試用時不要把「有文字輸出」當成合格。對表格與清單可核對列數及順序，對圖片與音訊確認是否需要額外套件或服務。若要處理整個資料夾，先清點檔案數與格式，再保存轉換失敗清單。

**很適合我，可以實際使用。**安裝與接入 Python 管線容易，適合先小量試驗。
