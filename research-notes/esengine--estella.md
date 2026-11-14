# Estella｜GitHub 專案導覽

> 專案：https://github.com/esengine/estella

## 1. 這是什麼？

Estella 是支援 2D、3D 的遊戲引擎，以 TypeScript SDK 撰寫遊戲邏輯，搭配 C++／WebAssembly 核心與獨立下載的視覺編輯器。README 列出網頁、桌面、微信小遊戲、互動廣告，以及 Android／iOS 的輸出目標，並說編輯器可透過 MCP 讓 Agent 操作。

## 2. 對我有什麼用？

若想用 TypeScript 製作同時有 2D 與 3D 內容的遊戲，可用一套編輯器與專案嘗試不同發行平台。也可研究 Agent 在視覺編輯器建立場景的工作方式；各平台的實際匯出與效能仍要自己測試。

## 3. 使用情境

- 製作含精靈、UI 與 3D 場景的遊戲原型。
- 先在網頁測試玩法，再評估桌面或行動裝置輸出。
- 讓 MCP 客戶端建立物件、設定元件並擷取畫面供人工驗收。

## 4. 我要怎麼用？

從 [下載頁](https://estellaengine.com/#download) 或 GitHub Releases 取得 Windows／macOS 編輯器。依 README 建立 New Project，在預設 Camera 場景加入物件，使用 TypeScript 元件與系統寫最小玩法，按 F5 預覽。確定基本流程後，再查官方文件的發行平台與 Agent MCP 連線指南；先以一個小作品驗證所需平台的輸出。

## 5. 值不值得研究？

若偏好 TypeScript 且需要跨平台 2D／3D 工作流程，值得用小型原型試用。README 對 MCP 工具數量有不同敘述，因此應以實際版本的編輯器和文件核對能力，不宜只根據功能表判斷成熟度。
