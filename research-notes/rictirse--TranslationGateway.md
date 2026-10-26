# Translation Gateway｜GitHub 專案導覽

> 來源：[rictirse/TranslationGateway](https://github.com/rictirse/TranslationGateway) README；查閱日期：2026-10-26。

## 1. 這是什麼？

Translation Gateway 是 Windows 桌面程式，配合 PotPlayer 把日文語音辨識結果或 YouTube 字幕即時翻成繁體中文。它組裝提示、呼叫你設定的 OpenAI 相容 LLM、以 OpenCC 轉換文字並快取結果。它也有術語卡、Whisper 辨識修正、字幕監看與編輯，支援直播與影片預先翻譯。

## 2. 對我有什麼用？

若你會看日文影片或直播，又希望在播放器內直接看到繁中字幕，它提供比逐句複製到翻譯器更連續的觀看方式。對人名、團體名、遊戲術語常被錯譯的內容，可建立術語卡；對語音辨識常聽錯的詞，則可審核後修正。若你平常很少看日文影音，導入成本可能不值得。

## 3. 使用情境

- 觀看日文 YouTube 影片，使用原有字幕或語音辨識再翻譯。
- 看日文直播，讓字幕持續顯示，並監看錯譯。
- 長期追同一實況主或作品時，累積專名與上下文設定。

## 4. 我要怎麼用？

README 要求 Windows 10/11 x64、PotPlayer 64-bit、.NET 10 Desktop 與 ASP.NET Core Runtime，以及可用的 OpenAI 相容 LLM 端點；直播另需 streamlink。先安裝 release 版本與依賴，在 Settings 設定模型 API Host、模型名稱和必要的金鑰，測試連線，再確認播放器路徑。複製 YouTube 或 Twitch 連結，按「Open video / stream」；第一次啟用時程式會寫入 PotPlayer 翻譯腳本與設定，字幕會出現在播放器及 Subtitle monitor。也可依 README 用 .NET SDK 從原始碼建置。先用短片測翻譯速度與品質，再處理直播。

## 5. 值不值得研究？

**經常看日文影音時值得試。** 它功能集中，但需要 Windows、PotPlayer 與自己的 LLM 端點；翻譯品質和費用取決於模型設定。
