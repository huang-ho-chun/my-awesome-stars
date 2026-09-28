# AI Agents: The Definitive Guide｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/Nicolepcx/ai-agents-the-definitive-guide/blob/main/README.md)；查閱日期：2026-09-28。

## 1. 這是什麼？

這是 O'Reilly 書籍《AI Agents: The Definitive Guide》的配套程式碼庫，依 12 個章節提供 Jupyter Notebook。內容從 LLM 到 Agent 的基礎，延伸到規劃、多 Agent、工具治理、部署、評估、記憶、成本與威脅模型。
它是跟著書本實作的教材庫，不是可直接部署的 Agent 框架。

## 2. 對我有什麼用？

你可以用它建立較完整的 Agent 工程知識地圖，尤其適合補足「做得出原型，但不知道怎麼評估、安全部署與控制成本」的部分。每章 Notebook 可直接在 Google Colab 開啟，因此不必先在 Windows 配好完整 Python 環境。
如果你只是想快速用現成 Agent，這個專案不會直接替你完成任務；它的價值在系統化學習與實驗。

## 3. 使用情境

- 初學 Agent：依章節理解 ReAct、規劃、工具呼叫和多 Agent 模式。
- 實作者：練習可靠執行、評估、觀測、記憶與成本設計。
- 團隊導讀：用 Notebook 當讀書會或內部訓練材料。
- 特定主題查漏：直接跳到安全、部署或威脅模型章節。

## 4. 我要怎麼用？

1. 先看 README 的章節目錄，挑選目前最需要的主題。
2. 點對應 Notebook 的 Colab 按鈕，在瀏覽器執行；需要模型服務的範例再配置自己的 API。
3. 對照書中說明修改範例輸入，記錄輸出與限制。
4. 若要本機執行，再複製倉庫並用 Jupyter 開啟各章 `.ipynb`；章節資料夾以 `CH01`、`CH02` 等命名。

## 5. 值不值得研究？

**適合系統化研究 Agent 工程。** 對你整理與使用各類 Agent 工具很有幫助，但最好搭配書本或選定章節逐步學，不必一次跑完全部 Notebook。
