# cangjie-skill 專案指南

來源：[kangarooking/cangjie-skill 官方 README](https://github.com/kangarooking/cangjie-skill/blob/HEAD/README.md)；查閱日期：2026-09-16。

## 1. 這是什麼？

把書籍、長影片與播客的方法萃取成可呼叫 Agent Skills 的流程。

## 2. 對我有什麼用？

你常把學到的技術方法轉成重複執行的工作規範；此專案可參考『來源→方法→可操作步驟』的拆解方式，但產出的 Skill 仍要人工校訂。

## 3. 使用情境

選一本有授權使用的技術資料，萃取出測試報告審查規則，讓 Agent 用新 Skill 處理一份舊報告；比較是否忠於原文與可重現。

## 4. 我要怎麼用？

README 將核心說明放在 SKILL.md 並提供不同宿主整合；先依對應平台安裝或複製 Skill，提供可合法使用的內容，檢查產出的索引、步驟與引用，再在真實樣本上試跑。

README 的核心不是把書縮成摘要，而是把可重複使用的方法整理成 callable Skill。可以對照產出 Skill 的步驟、來源片段與失敗條件，檢查是否真的能指導 Agent 做事。

## 5. 值不值得研究？

有特定情境才有用：有大量可重複的方法型資料要轉成 Skill 時值得研究。
