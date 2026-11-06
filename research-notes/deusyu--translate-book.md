# translate-book｜GitHub 專案導覽

> 專案：https://github.com/deusyu/translate-book

## 1. 這是什麼？

translate-book 是給 Codex、Claude Code 和 OpenClaw 使用的整書翻譯 Skill。它將 PDF、DOCX、EPUB 或 Markdown 轉成分段文字，交給多個子 Agent 並行翻譯，核對來源與譯文片段後合併，輸出 Markdown、HTML、DOCX、EPUB 和 PDF。

專案使用 manifest 與雜湊檢查片段完整性，支援中斷續跑、術語表、相鄰段落脈絡，以及術語變更後選擇性重譯。預設每批八個並行翻譯工作，但實際成本會隨書長、模型與環境變化。

## 2. 對我有什麼用？

適合將有合法使用權的長篇教材或書稿轉成可閱讀的另一種語言。分段、術語表與可續跑紀錄可幫助追蹤漏段和譯名變化；多種輸出格式便於在網頁、閱讀器與文件編輯器中檢查。它仍需要人工校閱重要概念、專有名詞和版面。

## 3. 使用情境

- 將授權的 EPUB 或 DOCX 書稿翻譯成中文供個人研讀。
- 對長篇技術材料建立一致術語表，分批完成翻譯。
- 在翻譯中斷後續跑，或針對術語變更的片段重譯。
- 將譯稿合併為 HTML、DOCX、EPUB 或 PDF 進行校對。

## 4. 我要怎麼用？

1. 備妥 Codex、Claude Code 或 OpenClaw，以及 Calibre、Pandoc、Python 3 和 `pypandoc`；README 提供安裝 Skill 的命令。
2. 提供來源檔路徑和目標語言，例如在 Codex 使用 `$translate-book Translate /path/to/book.pdf into Chinese.`。
3. Skill 會轉檔、分段、建立術語資訊、翻譯、驗證與合併；輸出預設在 `{book_name}_temp/`。
4. 核查 `output.md` 和產生的閱讀格式，必要時修正特定 `output_chunkNNNN.md` 後重新合併。

公式與表格密集的 PDF 可能被 Calibre 轉換打亂；README 建議先用 MinerU 或 Marker 抽取成 Markdown，再交給流程處理。首次使用宜從短篇且可公開使用的材料測試。

## 5. 值不值得研究？

若常處理長篇翻譯，值得研究其分段驗證、術語管理與續跑機制。它需要多個外部工具與 Agent 執行成本，且整書語意一致性仍有人工校閱需求；先以短篇測試來源轉換、譯文品質和輸出格式，再擴大到長書。
