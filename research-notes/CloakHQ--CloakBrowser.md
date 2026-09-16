# CloakBrowser 專案指南

來源：[官方 README.md](https://github.com/CloakHQ/CloakBrowser/blob/HEAD/README.md)｜查閱日期：2026-09-16

## 1. 這是什麼？

CloakBrowser 是改動 Chromium 指紋的瀏覽器及 Python/JavaScript 自動化套件，README 主打與 Playwright、Puppeteer 類似的程式介面，並有免費與 Pro 功能。它專注於避開反機器人偵測的場景。

## 2. 對我有什麼用？

你有瀏覽器測試與網頁資料流程，但一般合規的自動化任務可先用標準瀏覽器工具。它的額外複雜度、二進位下載與授權模式，對目前工作沒有明確必要。

## 3. 使用情境

若某個你有權測試的網站因指紋差異導致測試失真，先用可重現案例比較標準 Playwright 與此工具的行為，同時確認站方規則與測試範圍。

## 4. 我要怎麼用？

README 給出 `pip install cloakbrowser` 或 npm 路徑，並提供 Docker 測試指令。試用時先在隔離環境檢查二進位下載、license 和所需網路存取，再使用 Python `launch()` 或 Node API 跑最小測試；不要直接接私人登入資料。

## 5. 值不值得研究？

README 關於通過偵測的數字與展示是專案測試結果，不能視為任何網站都能穩定運作。導入會增加第三方瀏覽器版本、授權、更新和偵錯成本，應先有明確且獲授權的測試需求。

**對我目前用途不大。**只有特定授權測試被反自動化機制阻擋時才值得評估。
