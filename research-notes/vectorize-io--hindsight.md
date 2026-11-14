# Hindsight｜GitHub 專案導覽

> 專案：https://github.com/vectorize-io/hindsight

## 1. 這是什麼？

Hindsight 是供 AI Agent 儲存並運用長期記憶的服務。README 將記憶放在不同 bank 中，提供 `retain` 寫入、`recall` 查回、`reflect` 整理與推論三種操作；有 Docker 服務、Python／JavaScript 用戶端、MCP 與其他整合方式。

## 2. 對我有什麼用？

建立會跨多次對話工作的助理時，可以保存已確認的偏好、專案背景與過往經驗，讓後續任務能找回相關資訊。記憶 bank 可協助分開不同使用者或專案，但仍須自行決定何時寫入、如何更正與刪除過時內容。

## 3. 使用情境

- 為個人助理保留長期偏好，回答時查回相關記憶。
- 讓專案 Agent 記住已確認的決策與先前處理經驗。
- 比較普通檢索與 `reflect` 對需要綜合過往資訊問題的效果。

## 4. 我要怎麼用？

依 README 的 Quick Start，以 Docker 啟動服務並設定支援的 LLM 提供者，或試用 Python embedded 模式。先建立一個測試 bank，用 SDK 寫入少量已確認的資料，再執行 `recall` 與 `reflect`，核對是否忠於原始內容。正式使用前規劃資料權限、儲存位置、更新與刪除流程；README 亦列有自架及雲端選項，需選擇符合資料邊界的方式。

## 5. 值不值得研究？

需要持續學習的 Agent 記憶層時值得試驗。先用自己的問答資料比較回憶品質、延遲、成本及錯誤記憶的修正能力；README 的基準測試結果不能直接代表個人工作流程。
