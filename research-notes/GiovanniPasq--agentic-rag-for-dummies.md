# agentic-rag-for-dummies｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/GiovanniPasq/agentic-rag-for-dummies/blob/HEAD/README.md)；查閱日期：2026-09-16。

## 1. 這是什麼？

以 LangGraph 示範模組化 Agentic RAG 的教學專案。

## 2. 對我有什麼用？

README 展示 PDF 到 Markdown、分層索引、查詢釐清、對話記憶與人工參與。對你的 Obsidian 知識庫很有學習價值，但它是教學範例，需自行處理正式資料治理。

## 3. 使用情境

用一小批公開技術文件建索引，問跨文件問題並要求指出來源；觀察釐清步驟是否避免錯誤檢索，再核對原文。

## 4. 我要怎麼用？

先依 README 安裝 Python 相依套件並選 Ollama 或雲端模型，配置向量資料庫；將 PDF 轉 Markdown、建立分層索引，接著跑查詢流程。按章節逐步理解，比直接套入私人筆記庫更穩妥。

README 把文件前處理拆成 PDF 轉 Markdown 與分層索引，查詢端再做多階段處理和人工釐清。學習時分開測每段，能知道答案錯在解析、檢索還是生成。

## 5. 值不值得研究？

有特定情境才有用：若要親自設計 RAG 管線，這個範例很適合學結構；若只要現成檢索工具，可先用既有方案。
