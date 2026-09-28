# Hyper-Extract｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/yifanfeng97/Hyper-Extract/blob/main/README.md)；查閱日期：2026-09-28。

## 1. 這是什麼？

Hyper-Extract 是把 PDF、Office、HTML、EPUB 等非結構化文件轉成可查詢知識結構的 Python CLI。它支援一般分塊語料、清單、知識圖譜、超圖與時空圖等多種結構，並提供 80 多個 YAML 擷取範本。
它同時保留來源歸屬，可增量加入新文件、移除某份文件帶來的事實，並匯出成 Obsidian Markdown、GraphML、CSV 等格式。

## 2. 對我有什麼用？

這個專案和你的 Obsidian、來源保存及知識整理流程高度相關。你可以把一批文件先轉成帶來源的概念與關係，再匯出成含 `[[wikilinks]]` 的 Obsidian vault，作為人工整理前的草稿。
它也能透過唯讀 MCP 讓 Codex 或其他 Agent 搜尋、問答與匯出知識庫。不過擷取品質取決於文件解析、模型與範本，重要事實仍要回到原文核對。

## 3. 使用情境

- 研究資料整理：將多份報告抽成實體、事件和關係，保留每項資訊的來源。
- Obsidian 建庫：批次產生概念頁與雙向連結，再人工校正。
- 持續更新文件集：同一來源更新時重新餵入，管理舊事實的回滾。
- Agent 查詢：以 MCP 搜尋或詢問已整理的私有資料。

## 4. 我要怎麼用？

1. 安裝 `uv` 後以 `uv tool install hyperextract` 安裝 CLI，也可使用 `pipx`。
2. 選擇 LLM 與 embedding 供應商並執行設定；若要解析多種文件格式，安裝 ingestion 額外套件。
3. 先用少量文件與合適範本執行擷取，透過查詢和來源稽核檢查結果。
4. 確認品質後再擴大資料集；需要 Obsidian 時使用匯出功能，需要 Agent 存取時再安裝 MCP 額外套件並啟動 `he-mcp`。

## 5. 值不值得研究？

**很值得做小規模試驗。** 它符合來源可追溯、增量更新與 Obsidian 匯出的需求。先用幾份非敏感文件驗證中文解析與關係品質，再決定是否納入正式知識庫流程。
