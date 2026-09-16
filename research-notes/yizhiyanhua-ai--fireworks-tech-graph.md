# Fireworks Tech Graph（yizhiyanhua-ai/fireworks-tech-graph）

資料來源：[官方 README](https://github.com/yizhiyanhua-ai/fireworks-tech-graph/blob/HEAD/README.md)；查閱日期：2026-09-16。

## 1. 這是什麼？

把中英文自然語言描述轉為技術圖的 Agent Skill 與命令列工具。README 展示架構、流程、資料流等圖型及多種樣式，輸出可包含 SVG、PNG、動態圖或離線互動圖；也提供文字截斷檢查設定。它適合需要保持元件與連線可讀的技術圖，而不是一般統計圖表。

## 2. 對我有什麼用？

你常需要說明伺服器設定、Shell／Python 自動化與測試報告的流向，可用此工具快速產出給同事討論的草圖。中文標籤與輸出格式是優點；但架構圖的真實性仍由你提供元件、責任邊界與資料方向，不能只憑工具自動猜。

## 3. 使用情境

例如要交接客戶伺服器的報告流程，可以明確列出測試執行器、資料收集、清理、產報、人工審核與交付六個節點，以及每條箭頭的資料型態。先生成 SVG 檢查線條與文字有無遮蓋，再對照真實腳本修正關係，最後輸出 PNG 放進文件。

## 4. 我要怎麼用？

README 提供 Agent Skill 安裝、可編輯 Git checkout 和統一 CLI 三種路線；選一種即可。依 Installation 安裝完整 Skill，確認 Python 版本與 SVG 轉圖依賴（如 CairoSVG），需要動態輸出時再處理 Node／Puppeteer；Windows 路徑須按 README 的原生 Windows 說明調整。提供結構化描述後先生成 SVG，檢查完整標籤、連線與警告報告，再匯出所需格式。

## 5. 值不值得研究？

很適合我，可以實際使用：很貼合你需要說明測試與伺服器流程的工作；先從可人工校對的單張流程圖開始。
