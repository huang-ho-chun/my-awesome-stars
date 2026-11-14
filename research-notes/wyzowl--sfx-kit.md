# SFX Kit｜GitHub 專案導覽

> 專案：https://github.com/wyzowl/sfx-kit

## 1. 這是什麼？

SFX Kit 是 320 個原創音效及其描述資料的集合，涵蓋轉場、按鍵、提示、衝擊、生活物件等類別。每個音效提供 WAV 檔、適用與不適用情境、長度、同步點及音量資訊；README 說音效與資料以 CC0 提供，可用於商業作品。

## 2. 對我有什麼用？

製作影片、動畫或介面時，可以按畫面事件找音效，並利用同步點與音量欄位讓剪輯或 AI 工具更準確地放置聲音。完整資料也適合建立可搜尋的音效素材庫。

## 3. 使用情境

- 為畫面切換、按鈕點擊或標題出現挑選音效。
- 讓 Agent 讀取 `sounds.json`，依畫面事件、時長與避免使用條件挑候選聲音。
- 用同步點對齊剪輯畫面，再依旁白調整音量。

## 4. 我要怎麼用？

先瀏覽 [catalogue.md](https://github.com/wyzowl/sfx-kit/blob/main/catalogue.md) 或 `sounds/` 的類別，試聽候選檔。若讓工具自動挑選，先讀 [GUIDE.md](https://github.com/wyzowl/sfx-kit/blob/main/GUIDE.md) 與 `sounds.json`，用 `use_for`、`avoid_for`、`fits_seconds` 篩選；開始播放時間可按 README 的規則設為「畫面事件時間減 `sync.at`」。最後用實際播放檢查是否與旁白、音樂衝突。

## 5. 值不值得研究？

若常做短片或產品動畫，值得直接試幾個轉場和 UI 音效。素材可立即使用，且結構化欄位對自動剪輯有價值；真正合不合適仍要靠聆聽與混音判斷。
