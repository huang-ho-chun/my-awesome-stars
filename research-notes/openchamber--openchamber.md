# openchamber 專案指南

來源：[openchamber/openchamber 官方 README](https://github.com/openchamber/openchamber/blob/HEAD/README.md)；查閱日期：2026-09-16。

## 1. 這是什麼？

以 OpenCode 為核心的 Agent 開發工作環境。

## 2. 對我有什麼用？

提供桌面、瀏覽器/PWA、VS Code 與 CLI 形式，重點在持續目標、差異比較、遠端工作及排程。對你已有 Codex 的情況，主要是比較工作介面與協作方式。

## 3. 使用情境

在非客戶 repo 建立一個簡單的修正任務，測試 session 續作、變更審查與排程是否比現有流程更清楚；確認代理程式實際使用 OpenCode。

## 4. 我要怎麼用？

README 建議桌面版可從 Releases 安裝；VS Code 有擴充套件，CLI/Web 需要 Node.js 22 以上及 OpenCode CLI。選一種介面接入小型 repo，建立任務、檢查差異、試一次續作。

README 列出 desktop、VS Code、Web/PWA 和 CLI／Server 入口，底層使用 OpenCode。先選一種你會實際使用的入口，避免同時測遠端存取、排程與多裝置功能。

## 5. 值不值得研究？

有特定情境才有用：若需跨裝置或持續目標介面可試，否則現有 Codex 足以處理單次任務。
