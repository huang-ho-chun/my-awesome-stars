# Elephant-Goldfish Model

> 專案：[google/elephant-goldfish-model](https://github.com/google/elephant-goldfish-model)｜依據：專案 README（2026-10-28 查閱）

## 1. 這是什麼？

這是軟體設計與規格審查的 Agent Skills。『Elephant』掌握專案脈絡並起草方案，『Goldfish』從新對話視角審閱資料與草稿，找出沒有寫清楚的假設；最終取捨仍由使用者決定。

## 2. 對我有什麼用？

你在規劃測試系統、客戶環境部署或需跨模組修改時，可用它把需求與限制寫清楚，減少進入實作後才發現缺口。小型且明確的修正未必需要完整流程。

## 3. 使用情境

適合新增功能、架構取捨、多人協作或變更風險高的專案。例子是先釐清 webhook 失敗重試與重複事件，再寫規格。

## 4. 我要怎麼用？

按 README 選 Codex、Claude Code 或 Antigravity 安裝完整 plugin，重新開啟 session。對一個需要設計決策的功能先 brainstorm，接著 draft，再由獨立 reviewer 審查；依審查結果修正、核准規格後實作。此流程需要可建立新子 Agent 的環境。

## 5. 值不值得研究？

很適合你在較複雜的工程任務中使用。可先拿一個待規劃功能試一次，再評估是否納入固定流程。
