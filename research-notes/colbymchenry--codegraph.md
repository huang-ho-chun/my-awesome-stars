# codegraph｜研究說明

> 依先前對話重整的研究筆記，非逐字稿。專案功能可能隨版本改變。

**專案**：[colbymchenry/codegraph](https://github.com/colbymchenry/codegraph)

## 你當時問的重點

你想知道 CodeGraph 如何幫 Codex 理解現有程式庫。

## 先前說明

CodeGraph 先索引專案中的符號、呼叫關係與跨檔相依性，讓 Coding Agent 查「誰呼叫這個函式」「改這裡可能影響哪裡」等問題。它提供的是程式碼脈絡，並非另一個 Coding Agent；重點也不只是畫出關係圖。

## 對你的用處與用法

當你的測試腳本或報告流程跨越多個檔案時，可先建立索引，再請 Agent 查一條具體的呼叫路徑或變更影響範圍，與人工讀檔結果比對。

## 使用前要核對

索引可能落後於程式碼變更；重要修改仍要回到實際檔案和測試確認。
