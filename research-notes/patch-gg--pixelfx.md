# pixelfx｜GitHub 專案導覽

> 專案：https://github.com/patch-gg/pixelfx

## 1. 這是什麼？

pixelfx 是以 JavaScript 程式繪製的像素特效與動畫庫。專案目前收錄 244 個效果，涵蓋火焰、爆炸、水、冰、雷電、科幻、近戰、投射物、天氣、UI、轉場與小生物等分類；另外有 12 組把角色蓄力、命中停頓、目標反應和收招串起來的完整動作。

效果可以直接放進 Canvas、Phaser、PixiJS、Kaplay 或 three.js 網頁遊戲，也能匯出透明 Sprite Sheet 與對應 JSON，供 Godot、Unity、GameMaker、Defold、LÖVE、Bevy 等引擎使用。Repository 另附 Claude Code Skill，協助查找、套用、匯出或迭代製作新效果。

## 2. 對我有什麼用？

- 快速取得可改色、鏡像、旋轉且可重現的像素特效，不必從空白影格開始畫。
- 同一份程式效果可直接用於瀏覽器遊戲，也可轉成其他遊戲引擎較容易載入的素材表。
- 透過角色完整動作資料，參考攻擊前搖、命中停頓、擊退與恢復時間，而不只是貼上一段獨立特效。
- 使用內附工具反覆輸出接觸表、GIF、MP4 或 Sprite Sheet，檢查循環接縫、畫面溢出、未固定亂數與慢影格。
- 若使用 Claude Code，可把內附 Skill 當成建立和修整像素效果的工作流程範本。

## 3. 使用情境

- 為 2D 網頁遊戲加入火球、冰霜新星、治療光圈、命中閃光或道具拾取動畫。
- 將特效批次匯出為 Sprite Sheet，再導入 Godot 或 Unity。
- 替現有角色動作補上更清楚的蓄力、接觸停頓、受擊與收招節奏。
- 用不同色盤重用同一效果，例如把火焰改成藍焰或把治療光改成粉色。
- 研究如何以固定種子、顏色與發光緩衝區製作可重現的程式像素動畫。

## 4. 我要怎麼用？

1. 先開啟專案 Gallery 或 `docs/CATALOG.md`，依分類挑選效果。
2. 網頁專案可用 `npm i github:patch-gg/pixelfx` 安裝，或只複製需要的核心程式與效果檔。
3. 在 Canvas 遊戲中建立效果實例，逐幀呼叫更新與繪製；可傳入位置、方向、角度、種子與色盤等選項。
4. 其他遊戲引擎可執行 `node tools/render.mjs <效果名稱> --sheet`，輸出透明 PNG Sprite Sheet 與影格 JSON。
5. 要製作新效果時，可用 `node tools/new.mjs <分類/名稱>` 建立起點，再反覆執行 render 與 check 工具檢視及修正。
6. Claude Code 使用者可依 README 將 `pixelfx` 安裝成 Plugin 或複製 `skills/pixelfx`。

程式與效果採 MIT License；Gallery 使用的 Patch Pixel 字型不包含在相同授權內，使用前應查看專案的 `NOTICE.md`。

## 5. 值不值得研究？

值得，尤其適合想做 2D 遊戲、像素動畫或程式化視覺效果的人。它不只是素材包，還保留效果程式、匯出工具、角色動作資料與品質檢查流程，因此能同時作為可直接使用的資源和製作方法參考。

建議先挑一個現成效果，在瀏覽器中改色並匯出 Sprite Sheet，確認工作流程符合自己的引擎；若需要自製效果，再研究 Claude Code Skill 與 authoring 文件，避免一開始就承擔整套工具的學習成本。
