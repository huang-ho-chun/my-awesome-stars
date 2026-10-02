# patchright-enhanced｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/whaleyxbt/patchright-enhanced/blob/main/readme.md)；查閱日期：2026-10-02。

## 1. 這是什麼？

patchright-enhanced 是一個小型 TypeScript 瀏覽器自動化範本，使用 Patchright 啟動 Chrome，套用代理、時區、平行工作階段數量與起始頁面等設定。專案把 Patchright 內建的自動化特徵調整集中成可直接執行的框架，適合拿來建立 QA、網站監測或內部操作流程。

它目前的 README 只提供 Linux 設定方式。啟動後會開啟一個套用指定代理的 Chrome 工作階段並前往設定的起始網址，瀏覽器會持續開啟，直到使用者手動關閉。這不是完整的爬蟲產品，也沒有提供現成的網站操作腳本、排程、資料儲存或監控介面。

## 2. 對我有什麼用？

如果你需要用真實瀏覽器做網站流程測試、定期檢查頁面，或在內部工具中重複操作登入後的網站，它可以作為比從零建立 Patchright 專案更快的起點。環境變數已整理出 Chrome 路徑、瀏覽器時區、最大平行數量與起始頁面，代理則從 `proxies.txt` 讀取。

對你目前的 Windows 環境而言，直接價值有限，因為官方說明以 Linux 與 `/usr/bin/google-chrome-stable` 為預設。若要使用，較合理的方式是在 WSL、Linux 主機或容器中先試跑，而不是直接假設能在 Windows 原生環境無修改運作。

## 3. 使用情境

- **內部網站 QA**：開啟不同代理或時區的瀏覽器，檢查頁面是否正常。
- **網站可用性監測**：在自己的測試環境中定期走固定頁面或操作流程。
- **跨地區驗證**：使用合法取得的代理檢查網站在不同區域的顯示結果。
- **Patchright 實驗起點**：研究其與 Playwright 的差異，再加入自己的測試或資料擷取邏輯。

## 4. 我要怎麼用？

1. 在 Linux 環境準備 Node.js、npm 與 Chrome，再執行 `npm install`。
2. 使用 `npx patchright install chrome` 安裝 Patchright 所需的瀏覽器元件。
3. 將 `.env.example` 複製成 `.env`，設定 Chrome 路徑、時區、最大平行數與起始網址。
4. 依 README 格式將代理寫入 `proxies.txt`；若不需要代理，先查看程式與範例是否允許空白設定。
5. 執行 `npm run build` 和 `npm start`，確認 Chrome 能以預期設定開啟。
6. 再加入自己的 QA 或監測步驟。操作第三方網站時，應遵守網站條款、授權範圍與存取限制。

## 5. 值不值得研究？

**只有特定瀏覽器自動化需求時值得研究。** 它的程式範圍小，適合快速理解 Patchright 的啟動與代理設定；但文件簡短、目前偏 Linux，也沒有完整工作流程。若你只是要做一般網站自動化，現有 Playwright 或已配置的瀏覽器工具通常更直接；需要 Patchright 特性時再收藏並試驗。
