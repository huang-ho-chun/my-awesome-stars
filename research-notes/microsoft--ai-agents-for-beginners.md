# AI Agents for Beginners｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/microsoft/ai-agents-for-beginners/blob/main/README.md)；查閱日期：2026-09-29。

## 1. 這是什麼？

AI Agents for Beginners 是微軟提供的入門課程，以 18 課文字教材、短影片與 Python 範例介紹如何建立 AI Agent。內容從 Agent 使用情境和框架開始，延伸到設計模式、工具使用、Agentic RAG、可信任性、規劃、多 Agent、記憶、MCP／A2A／NLWeb、上下文工程、正式環境部署、本機 Agent 與安全。

它是結構化學習課程，不是可以直接拿來完成工作的 Agent 產品。程式範例目前以 Microsoft Agent Framework 與 Microsoft Foundry Agent Service V2 為主，部分範例可使用其他 OpenAI 相容模型服務。

## 2. 對我有什麼用？

你可以用它補齊目前收藏中各種 Agent 工具背後的共同觀念，理解工具呼叫、規劃、記憶、上下文、協定、部署和安全之間的關係。這能幫助你判斷一個 Agent 專案只是展示功能，還是已考慮可靠性、評估與正式環境需求。

每課同時提供文字、影片和程式範例，適合依自己的時間分段學習。不過要完整執行主要範例，通常需要 Azure 帳號與 Microsoft Foundry；如果只想理解概念，可以先讀教材和觀看影片，不必立即申請或付費。

## 3. 使用情境

- **第一次系統學 Agent**：從基本定義、使用情境和框架開始建立完整地圖。
- **補強特定主題**：直接閱讀工具使用、Agentic RAG、記憶、上下文工程或安全等章節。
- **做小型實作**：跟著 Python 範例建立 Agent，觀察工具、規劃與多 Agent 流程。
- **評估正式導入**：用可信任性、部署、擴充與安全章節檢查自己的 Agent 專案。
- **比較框架與服務**：了解 Microsoft Agent Framework 和 Foundry Agent Service 的定位，再與其他收藏工具比較。

## 4. 我要怎麼用？

1. 先從 README 的 18 課目錄選擇學習順序。若對生成式 AI 還不熟，可先看專案推薦的 Generative AI for Beginners。
2. 每課先讀該資料夾的 README，再看短影片；只想了解概念時可以先略過程式碼。
3. 要執行範例時，先閱讀 `00-course-setup` 的設定文件，準備 Python 環境、複製倉庫，並依範例需求設定 Microsoft Foundry 或相容模型服務。
4. 每完成一課，用自己的情境改寫一個小範例並記錄限制，例如工具失敗、成本、權限或資料來源。
5. 不需要照順序一次學完；可優先學工具使用、Agentic RAG、記憶、上下文工程和安全，再回頭補其他章節。

## 5. 值不值得研究？

**很適合你作為 Agent 入門到實務的系統課程。** 它的主題完整，也能連結你已收藏的 Agent、RAG、MCP 與記憶工具。建議先以文字與影片建立觀念，再挑 2 至 3 個最相關章節實作；若不打算使用 Azure，程式範例的直接價值會降低，但教材本身仍值得閱讀。
