# instaloader｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/instaloader/instaloader/blob/HEAD/README.rst)；查閱日期：2026-09-16。

## 1. 這是什麼？

Instaloader 是 Instagram 下載 CLI，官方 README.rst 說可下載公開或經授權登入可見的媒體、標題、留言、地理標記等，並支援中斷續傳與更新。它不是分析器，也不保證平台內容始終可取得。

## 2. 對我有什麼用？

你已有私人 Instagram 封存工作，它可作核對媒體與中繼資料的輔助工具；但登入時會有 session 檔，應注意儲存位置與帳號安全。原始匯出和既有清單仍要保留。

## 3. 使用情境

只對自己的帳號或明確有權處理的少量內容試下載，對照平台匯出：媒體數、日期、caption、留言和檔名是否一致，再決定是否補足缺口。

## 4. 我要怎麼用？

README 以 `pip3 install instaloader` 安裝；公開測試可執行 `instaloader profile`，增量更新有 `--fast-update` 或 `--latest-stamps`。需登入時參考 `--login` 說明，先確認 session cookie 檔保存方式，不把帳密或 session 放進專案。

## 5. 值不值得研究？

Instagram 的可見內容和下載行為可能隨平台調整而改變。試用時以「已取得媒體數、缺漏項目、失敗原因」做對照表；若出現登入驗證或異常提示，應停止自動化，改用官方匯出與既有備份核對。

**有特定情境才有用。**可補充 IG 封存，但現有匯出與人工核對更能作主資料來源。
