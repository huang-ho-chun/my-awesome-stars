# markdown-online-editor 專案指南

來源：[官方 README.md](https://github.com/nicejade/markdown-online-editor/blob/HEAD/README.md)｜查閱日期：2026-09-16

## 1. 這是什麼？

Arya 是瀏覽器中的 Markdown 編輯器，README 列出即時預覽、流程圖、甘特圖、時序圖、ECharts、簡報預覽、HTML 轉 Markdown，以及匯入匯出多種格式。它偏向編輯與排版，不是 Obsidian 筆記庫管理工具。

## 2. 對我有什麼用？

寫公開技術說明或臨時把內容排成報告時可用；但私人筆記和社群資料若貼進線上服務，需先確認本機儲存行為與內容去向。你現有 Obsidian 編輯流程不一定需要替換。

## 3. 使用情境

用一篇非敏感 Markdown 草稿試流程圖和 PDF 匯出，對照原 Markdown 的表格與連結是否保持可讀；再看看所見即所得編輯是否保留你常用語法。

## 4. 我要怎麼用？

可直接開 README 指向的線上編輯器；想控制資料可依 Docker 範例自架，將容器對應本機連接埠後開啟網頁。專案也提供原始碼部署方式。先用測試草稿，匯出後檢查檔案與暫存。

## 5. 值不值得研究？

若只是想分享格式化報告，可把它當輸出前的預覽工具；若要長期編修筆記，還需確認 Obsidian wikilink、callout 與 frontmatter 在匯入匯出後是否保留。未驗證前不宜把主 Vault 複製進編輯器。

**有特定情境才有用。**報告排版或分享時有用，日常 Obsidian 筆記仍可沿用現有工具。
