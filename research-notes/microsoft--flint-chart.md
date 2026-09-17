# flint-chart｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/microsoft/flint-chart)；查閱日期：2026-09-16。

## 1. 這是什麼？

Flint 是給開發者與 AI Agent 使用的圖表描述層。Agent 描述資料欄位的**意義**、想比較的項目與圖表形式，Flint 再處理版面、刻度、標籤、圖例和風格，輸出給 Vega-Lite、ECharts、Chart.js、Plotly 或 Excel 等後端。它不是取代所有圖表函式庫，而是減少 Agent 每次從頭決定細部設定。

## 2. 對我有什麼用？

你的效能測試和自動報告流程常需要把多組結果畫成圖。你可以給 Agent 一份有 GPU 型號、吞吐量或頻寬欄位的資料，讓它用 Flint 產生比較圖，再把圖放進報告。它的 semantic types 可協助表達欄位代表價格、溫度、排名等含義；但單位和數據解讀仍由你檢查。

## 3. 使用情境

- **快速試圖**：透過 MCP 讓 Agent 對公開或測試資料生成圖表。
- **報告產線**：開發者用 JavaScript／TypeScript 套件把同一份圖表描述輸出到不同圖表後端。
- **統一風格**：在多張圖共用 theme，減少標籤、間距和顏色各自不一致。

## 4. 我要怎麼用？

1. 先選路線。若只想看 Agent 做圖，README 提供 [MCP 試用方式](https://github.com/microsoft/flint-chart#try-it-in-your-agent)；若要接入程式，安裝 `flint-chart` 套件；本機 MCP 也有 `flint-chart-mcp`。
2. 取一份小型 CSV，明確告訴 Agent 各欄位含義、單位及比較目的，先產生一張圖。
3. 對照原始資料檢查刻度、聚合、單位和圖例；滿意後再接進你的自動報告流程。

## 5. 值不值得研究？

**有特定情境時很適合你。** 當你要讓 Agent 反覆產生多張一致的測試圖表時值得研究；偶爾只畫一張簡單圖，現有工具已足夠。
