# OpenCLI｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/jackwener/OpenCLI/blob/main/README.md)；查閱日期：2026-09-24。

## 1. 這是什麼？

OpenCLI 是把網站功能轉成命令列操作的工具，也能透過 Chrome／Chromium 的 Browser Bridge 擴充功能，讓 AI Agent 使用你現有瀏覽器中的登入狀態。它提供多個網站的現成指令，也能建立私人 adapter、修復失效 adapter，或以瀏覽器命令臨時導航、點擊、填表與擷取資料。

它比較像**網站操作與 Agent 之間的轉接層**。桌面使用者可裝 OpenCLIApp；伺服器或 CI 也能使用純 CLI 安裝，但需要 Node.js 20.18.1 以上。

## 2. 對我有什麼用？

你會讓 Codex 查 GitHub、網頁與社群資料。OpenCLI 可把已登入網站的讀取流程變成穩定、可重複的命令，減少每次都靠畫面座標操作。若某網站沒有官方 API，或 API 很難設定，它能讓 Agent 透過你控制的瀏覽器讀取頁面與網路回應。

它特別適合建立固定查詢，例如查看通知、搜尋內容或擷取清單。涉及發文、按讚、追蹤和訊息等寫入動作時，仍應要求 Agent 先取得明確授權；共用瀏覽器登入狀態也代表工具能接觸該帳號可見的資料，需要慎選 adapter 和權限。

## 3. 使用情境

- 用結構化命令讀取已登入網站的搜尋結果、貼文或通知。
- 為常用網站建立可重複的私人 adapter。
- adapter 因網站改版失效時，使用 autofix Skill 協助修復。
- 讓 Agent 臨時控制真實頁面，完成導航、填表或資料擷取。
- 用多個 Chrome profile 別名分開工作與私人帳號。

## 4. 我要怎麼用？

Windows 最省事的起點是安裝 OpenCLIApp，再安裝官方 Browser Bridge 擴充功能，執行 `opencli doctor` 確認連線，最後先跑 `opencli list` 和一個不需登入的唯讀指令。需要 Agent 操作時，再安裝專案提供的 OpenCLI Skills。

建議一開始使用獨立 Chrome profile，只測試唯讀工作。確認它選到正確 profile、輸出內容符合預期後，再逐步增加需要登入的網站。純命令列環境可以用 npm 安裝，但瀏覽器型指令仍需要可用的 Browser Bridge 或 CDP 連線。

## 5. 值不值得研究？

**很適合我，可以實際使用。** 它可補強 Agent 對網站和登入內容的讀取能力，也能把常用流程做成命令。不過應先從獨立 profile 與唯讀指令開始，避免一開始就開放帳號寫入操作。
