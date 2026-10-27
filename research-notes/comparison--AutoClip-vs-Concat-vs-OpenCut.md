# AutoClip vs Concat vs OpenCut：三個開源影片工具怎麼選？

> 更新日期：2026-10-27

這三個專案都和影片剪輯有關，但其實不是完全相同的產品。最重要的差別可以先記成一句話：

- **AutoClip**：AI 幫你決定「哪一段值得剪」，重點是把長影片自動變成短影音。
- **Concat**：你決定「要怎麼剪」，是一套現在就能使用的本機開源影片剪輯器。
- **OpenCut**：同樣走開源 CapCut 替代路線，但新版正在從頭重寫，現在更適合追蹤它未來的 Plugin、MCP 與自動化能力。

如果現在只想實際安裝兩個，最合理的組合是：

> **AutoClip + Concat**

前者負責 AI 找精華與快速產生短影音，後者負責手動微調與一般影片剪輯；OpenCut 則先收藏、等新版成熟。

---

## 1. 快速比較

| 項目 | AutoClip | Concat | OpenCut |
| --- | --- | --- | --- |
| 核心定位 | AI 長影片轉短影音 | 完整本機影片剪輯器 | 開源、可擴充的影片剪輯平台 |
| 最像什麼 | OpusClip 類型工具 | CapCut 開源替代品 | CapCut 開源替代品 |
| 誰決定剪什麼 | **AI** | **使用者** | **使用者** |
| 主要輸入 | YouTube、Podcast、訪談、課程等長影片 | 本機影片、圖片、音訊 | 影片、圖片、音訊 |
| 主要輸出 | 短影音、字幕、封面、發布文案 | 完整剪輯後的影片 | 完整剪輯後的影片 |
| Timeline 手動剪輯 | 有，但不是核心 | 核心功能 | 核心功能 |
| AI 的角色 | 核心 | 輔助剪輯與 Agent 控制 | 未來的 Agent / Plugin 能力 |
| 自動找精華 | **核心能力** | 不是主要定位 | 不是主要定位 |
| 本機 / 隱私 | 剪輯與渲染在本機，部分雲端模型按量使用 | **強調 100% local / offline** | 強調隱私與跨平台、本機核心方向 |
| MCP | 已有 | 已有 | 規劃中 |
| 其他自動化 | CLI | JSON-RPC API | 規劃 Headless、Batch Rendering、Scripting |
| 現況 | 可直接使用 | Beta，但已能實際剪片 | **主線正在重寫** |
| 現在最適合 | 自動做 Shorts / Reels | 家庭影片、一般剪輯、精細控制 | 收藏、追蹤未來平台發展 |

---

# 2. 真正的分界：誰負責「剪輯決策」？

這是三個工具最重要的差異。

## AutoClip：AI 幫你選內容

AutoClip 的核心不是提供一條更漂亮的 Timeline，而是減少「我要先把整支影片看完，才能知道哪裡值得剪」這件事。

典型流程是：

```text
長影片 / YouTube / Podcast / 訪談
                ↓
             AutoClip
                ↓
          AI 理解影片內容
                ↓
          找出值得剪的片段
                ↓
       重新裁切成短影音比例
                ↓
      字幕 / 封面 / 發布文案
                ↓
     Shorts / Reels / TikTok
```

所以它適合的是：

- Podcast 精華
- 訪談精華
- YouTube 長影片再利用
- 課程重點片段
- 社群短影音內容生產

例如看到一支 2 小時的 AI 訪談，你不需要自己先找出 `37:12～38:05` 哪一段最好，AutoClip 的價值就在於先替你做這層內容判斷。

### AutoClip 的關鍵價值

不是「剪輯功能比 CapCut 多」，而是：

> **降低從長影片找到值得發布片段的人工時間。**

---

## Concat：你知道要剪什麼，它負責讓你剪出來

Concat 的定位比較接近傳統影片編輯器。

你自己決定：

- 哪裡切掉
- 哪裡保留
- 哪段放大
- 字幕怎麼呈現
- 要不要加轉場
- 音樂放在哪
- 圖片放哪一軌
- 最後輸出什麼格式

Concat 提供的是完整的剪輯環境，包括：

- 多軌 Timeline
- Split / Trim / Merge
- Keyframe
- Transition / Effects
- Titles
- Whisper 自動字幕
- Text-to-Speech
- Voice Cloning
- Background Removal
- Audio Cleanup
- H.264 / HEVC / AV1
- 最高 4K 60fps 輸出

所以它更像：

> **免費、開源、本機優先的 CapCut。**

如果要剪家庭影片、寶寶成長紀錄、旅遊紀錄，或已經知道自己要留下哪些片段，Concat 比 AutoClip 合適很多。

---

## OpenCut：和 Concat 同類，但目前還在「重造剪輯平台」

OpenCut 和 Concat 才是真正比較接近的競爭者。

它同樣希望提供一套免費、開源、簡單的 CapCut 替代方案，但目前最大的差異是：

> **OpenCut 新版正在從頭重寫。**

官方目前列出的新版方向包括：

- Editor API
- Plugin-first architecture
- Third-party plugins
- Rust core
- Desktop / Mobile / Browser 共用核心
- MCP Server
- Headless mode
- Batch rendering
- Editor 內建 scripting tab

因此 OpenCut 未來可能不只是一套剪輯軟體，而比較像：

> **可以被 Plugin、Script 與 AI Agent 擴充的影片編輯平台。**

這是它最值得關注的地方。

但現階段必須注意：

- 主 repo 是新版重寫中的版本。
- 官方仍建議真正要使用的人先使用 Classic。
- `opencut-classic` 已經 Archived，不再維護。

因此現在拿它當唯一主力剪輯器並不是最理想的選擇。

---

# 3. Concat vs OpenCut：兩個開源 CapCut 替代品怎麼選？

這兩個才適合直接放在一起比較。

## Concat 的方向

比較偏：

> **Local-first 的完整桌面剪輯器。**

重點是：

- 現在就可以下載使用
- 功能已經很多
- 強調影片不離開本機
- AI 模型下載後可離線使用
- 已有 MCP
- 已有 JSON-RPC API

所以現在如果問：

> 「我今晚就要剪一支影片，該裝哪個？」

答案比較偏向 **Concat**。

---

## OpenCut 的方向

新版比較偏：

> **可程式化、可擴充、跨平台的影片編輯平台。**

Plugin-first 架構尤其值得注意。

理想上未來可能形成：

```text
OpenCut
│
├─ 基本剪輯
├─ Subtitle Plugin
├─ AI Plugin
├─ YouTube Plugin
├─ 自動剪輯 Plugin
└─ 自訂 Plugin
```

再加上：

```text
MCP
Headless
Batch Rendering
Scripting
Editor API
```

它未來可能比「CapCut clone」更像影片版的可擴充工作平台。

但這些目前仍以新版 roadmap / 開發方向為主，不能當成已經成熟的功能。

---

# 4. AI 在三者裡的角色不同

很容易因為三個專案都提到 AI / MCP，而以為它們差不多。

其實完全不同。

## AutoClip

```text
AI = 核心產品
```

沒有 AI，自動找精華與內容再利用的核心價值就不存在。

AI 負責：

- 理解內容
- 選片段
- 整理短影音
- 字幕
- 標題 / 封面 / 發布文案

---

## Concat

```text
影片剪輯器 = 核心
AI = 加值能力
```

就算完全不用 AI，Concat 還是一套可以正常使用的影片編輯器。

AI / MCP 比較像是：

> 讓 Agent 幫你控制剪輯器。

---

## OpenCut

```text
影片編輯平台 = 核心
AI / MCP / Plugin = 未來擴充層
```

它最有意思的不是目前有多少 AI 功能，而是如果 Plugin、Editor API、MCP、Headless 都成熟後，AI Agent 可能更容易把整套剪輯工作流程串起來。

---

# 5. MCP 的差別

## AutoClip MCP

比較接近工作流層級：

```text
「把這支訪談剪成 3 支 Shorts」
            ↓
          Agent
            ↓
         AutoClip
            ↓
   找內容 / 剪片 / 字幕 / Render
```

適合「給一個目標，讓系統完成整段內容再利用流程」。

---

## Concat MCP

比較接近剪輯器操作層級：

```text
「刪掉 15～25 秒」
「第二軌放這張圖片」
「幫我加字幕」
「把人物放大」
            ↓
          Agent
            ↓
          Concat
```

也就是讓 AI 操作真正的 Timeline。

---

## OpenCut MCP

目前仍屬新版規劃方向。

如果之後和 Editor API、Plugin、Headless、Scripting 整合成熟，可能形成非常完整的 Agent 剪輯環境。

因此它現在比較適合：

> **觀察與追蹤，而不是因為 MCP 就直接換過去。**

---

# 6. 實際使用情境怎麼選？

| 使用情境 | 建議 |
| --- | --- |
| 2 小時 Podcast 自動抓 5 個精華 | **AutoClip** |
| YouTube 訪談轉 Shorts / Reels | **AutoClip** |
| AI 影片內容再利用 | **AutoClip** |
| 不想自己找值得剪的時間點 | **AutoClip** |
| 寶寶成長紀錄 | **Concat** |
| 家庭影片 | **Concat** |
| 生產紀錄 / 旅遊紀錄 | **Concat** |
| 自己控制字幕、音樂、轉場、畫面 | **Concat** |
| 私人影片不希望上傳雲端 | **Concat** |
| 想找現在能用的開源 CapCut | **Concat** |
| 想研究可擴充影片剪輯平台 | **OpenCut** |
| 想關注 Plugin-first 剪輯架構 | **OpenCut** |
| 想研究未來 MCP + Headless + Script | **OpenCut** |

---

# 7. 可以搭配使用，而不是只能三選一

AutoClip 和 Concat 其實非常互補。

最實際的工作流是：

```text
長影片
   ↓
AutoClip
AI 找精華 / 初步裁切 / 字幕
   ↓
短影片素材
   ↓
Concat
手動修剪 / 字幕微調 / 音樂 / 特效
   ↓
最終成片
```

因此它們不像傳統意義上的「競品二選一」。

真正比較像競品的是：

```text
Concat  ←→  OpenCut
```

而：

```text
AutoClip
```

比較像前端的 AI 內容再利用工具。

---

# 8. 現在應該怎麼選？

## 如果只想裝一個

### 想讓 AI 幫你剪

選 **AutoClip**。

適合：

- 長影片很多
- 常看 YouTube / Podcast
- 想快速做短影音
- 不想花時間手動找精華

---

### 想自己剪影片

選 **Concat**。

適合：

- 家庭影片
- 寶寶影片
- 一般 Shorts
- 旅遊紀錄
- 私人影片
- 想找免費 CapCut 替代品

---

### 對 OpenCut 很有興趣

現在先 **Star / 收藏追蹤**。

等新版至少把：

- Desktop
- Editor API
- Plugin
- MCP
- Headless

等主要能力穩定後，再重新和 Concat 比較會比較合理。

---

# 9. 對我的實際建議

## AutoClip：★★★★★ 很適合實際使用

最符合目前常見的 YouTube、AI 資訊、Podcast、長影片整理與內容再利用情境。

它最大的價值不是取代一般剪輯器，而是把：

> 「看完整支影片 → 找精華 → 剪片」

縮短成 AI 協助完成的流程。

---

## Concat：★★★★☆ 值得安裝

如果開始整理：

- 寶寶影片
- 家庭紀錄
- 旅行影片
- 短影音

它會比 AutoClip 更實用。

而且 Local-first 對私人家庭影片尤其有價值。

---

## OpenCut：★★★★☆ 先收藏追蹤

目前不建議因為功能願景就把它當主力剪輯器，但新版的：

- Plugin-first
- MCP
- Editor API
- Headless
- Scripting

都很值得繼續觀察。

如果這些方向成功落地，它未來可能不只是「另一個 CapCut 替代品」，而是一個可被 AI Agent 與自動化工作流深度控制的剪輯平台。

---

# 10. 最後結論

最簡單的判斷方式：

```text
AI 幫我決定「剪什麼」
→ AutoClip

我知道我要什麼，自己控制「怎麼剪」
→ Concat

我想追蹤未來可程式化、Plugin-first、AI Agent 友善的剪輯平台
→ OpenCut
```

目前最實際的組合：

> **AutoClip + Concat**

目前最值得持續追蹤的變化：

> **OpenCut 新版是否能把 Plugin + MCP + Headless + Scripting 真正做成熟。**

---

## Repository

- [AutoClip](https://github.com/zhouxiaoka/autoclip)
- [Concat](https://github.com/jub0t/Concat)
- [OpenCut](https://github.com/OpenCut-app/OpenCut)
