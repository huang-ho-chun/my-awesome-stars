# lieflat-charts｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/larashero3-dotcom/lieflat-charts/blob/HEAD/README.md)；查閱日期：2026-09-16。

## 1. 這是什麼？

符合 Agent Skills 格式的資料視覺化與 HTML 報告 Skill。README 區分單張圖與報告模式：一般資料先產出圖，只有使用者明確要求報告、月報、白皮書等才使用整頁模板。內含 Lupi、Glance、Basics 等不同閱讀節奏的圖型與互動大圖，可調整統一配色與版面。

## 2. 對我有什麼用？

你已有測試結果與報告管線，這項工具可把 CSV 或整理後的指標轉成更易讀的 HTML 圖表。它對主管簡報前的週報、失敗率走勢或測試覆蓋範圍有直接用途，但視覺品質不能取代數據驗證。圖中的單位、排序與來源都應回對原始資料。

## 3. 使用情境

例如每週測試報告有通過數、失敗數和延遲變化，可先請 Codex 用 Glance 型式呈現異常，再以 Lupi 補充逐項紀錄。交付前把圖上的分母、時間範圍與每個註記對照 CSV；若某種美化讓小變化看起來巨大，就調整量尺或文字說明。

## 4. 我要怎麼用？

可先到 README 的 Preview 看圖型。最少可在 Moxt 中使用；若要裝到相容 Agent，README 提供 `npx skills add https://github.com/larashero3-dotcom/lieflat-charts --skill lieflat-charts`。安裝後把資料、想回答的問題、讀者與輸出格式交給 Agent，明確要求圖或整頁報告，檢查產出的 HTML 與原始值。Skill 安裝不等於資料自動接入現有管線，先用一份樣本。

## 5. 值不值得研究？

很適合我，可以實際使用：可直接改善測試報告的可讀性；導入時先建立數值與來源核對步驟。
