# CodeGraph｜給 AI Coding Agent 使用的本地程式碼關係圖

> 來源：[colbymchenry/codegraph](https://github.com/colbymchenry/codegraph)

- 類型：Developer Tool / Code Knowledge Graph / MCP 工具
- 適合搭配：Codex CLI、Claude Code、Cursor、Gemini CLI、OpenCode、GitHub Copilot、Kiro 等
- 對我的判斷：**很適合，可以實際試用**

## 1. 這是什麼？

一句話來說：

> **CodeGraph = 先把整個程式專案建立成「程式碼關係圖」，讓 Codex / Claude Code / Cursor 不需要每次都靠 grep、讀一堆檔案來理解專案。**

它不是另一個 AI coding agent，而是**幫 coding agent 提供更精準 codebase context 的基礎工具**。

假設專案：

```text
report_implement/
├── AGENTS.md
├── pod_report/
│   ├── build_report.py
│   ├── md_to_pdf.py
│   └── src/
│       ├── run.py
│       ├── cpu.py
│       ├── gpu.py
│       └── network.py
└── tests/
```

如果問 Codex：

> 「幫我修改 GPU report 的產生流程，但不要影響 PDF pipeline。」

正常情況下，AI 可能必須自己探索：

```text
grep GPU
↓
讀 run.py
↓
發現呼叫 gpu.py
↓
讀 gpu.py
↓
找誰呼叫 run.py
↓
讀 build_report.py
↓
找 PDF pipeline
↓
讀 md_to_pdf.py
↓
開始理解關係
```

這就是 Coding Agent 很常見的：

**Search → Read → Search → Read → Search → Read**

CodeGraph 的想法則是先做：

```text
codegraph init

            build_report.py
                  │
                  ▼
               run.py
             /    │    \
            ▼     ▼     ▼
         cpu.py gpu.py network.py
                  │
                  ▼
             output.md
                  │
                  ▼
            md_to_pdf.py
```

它會建立包含 **symbol、call edge、dependency、cross-file relationship** 等資訊的 graph。

之後 Agent 可以直接查：

- GPU report 相關 code 在哪？
- 誰呼叫這個 function？
- 這個 function 呼叫哪些東西？
- 改這裡可能影響哪些地方？
- A 到 B 的 call path 是什麼？

而不是每一次都重新探索整個 repository。

---

## 2. 它真正有價值的地方：不是畫圖

名字叫 CodeGraph，很容易讓人以為：

> 「就是把 code 畫成 dependency graph。」

其實**重點不是 UI，而是給 AI Agent 使用。**

整體概念比較像：

```text
你的 Code
   ↓
CodeGraph Index
   ↓
Code Knowledge Graph
   ↓
MCP
   ↓
Codex / Claude Code / Cursor
```

CodeGraph 可以作為 Coding Agent 理解 repository 的額外工具。

這也是為什麼它跟我目前的使用方式關係很大。

我現在大量使用：

```text
Codex
+
AGENTS.md
+
專案說明文件
+
AI 協作開發
```

CodeGraph 正好補另外一塊：

```text
AGENTS.md
「這個專案應該怎麼工作」

設計文件
「為什麼當初這樣設計」

CodeGraph
「程式現在實際上怎麼連在一起」

Git / commit
「程式怎麼演變成現在這樣」
```

這四個其實是在解決不同問題。

---

## 3. 對我最有用的功能

### 3.1 讓 Codex 更快理解既有專案

例如現在的 report pipeline。

可能會問：

> 修改 `build_report.py` 的某段邏輯。

Codex 原本可能先花很多 context：

```text
read
grep
read
grep
read
...
```

CodeGraph 的設計，就是讓 agent 可以更直接取得 relevant context。

作者自己的 benchmark 宣稱，在七個 repository 上平均：

- token 約減少 62%
- cost 約降低 44%

不過這是**專案作者自己的 benchmark**，不能直接理解成使用 Codex 時一定會得到相同幅度。

真正效果仍然會受到 repository 大小、codebase 結構、語言、cross-file dependency 複雜度、問題本身，以及 Coding Agent 原本 code search 能力影響。

對我而言，比省 token 更重要的其實可能是：

> **減少 Codex 看漏 dependency。**

### 3.2 Impact Analysis

這可能反而是我最值得使用的功能。

例如準備修改：

```text
generate_gpu_report()
```

CodeGraph 可以從 graph 找出：

```text
generate_gpu_report
        ↑
      run.py
        ↑
 build_report.py
        ↑
   report pipeline
```

也就是協助回答：

> **「改這裡可能影響到哪裡？」**

README 將這類功能描述成 change 的 **blast radius / impact radius**。

這跟我原本的工程工作方式其實非常接近。以前 Firmware / Kernel debug 很常做的事情，本質上就是：

```text
這個 function 是誰 call？
↓
這個 value 從哪裡來？
↓
改這個 property 哪些地方受到影響？
↓
哪條 execution path 會走進來？
```

CodeGraph 等於把這種思考方式做成 Agent 可以直接查詢的工具。

因此它的價值不只是「AI 找 code 比較快」，更重要的是：

> **AI 在修改 code 之前，可以更有系統地確認影響範圍。**

### 3.3 Codebase 視覺化

也可以直接執行：

```bash
codegraph ui
```

然後從瀏覽器查看本地 UI。

README 描述的介面概念大致是：

```text
Callers
   │
   ▼
Current Symbol
   │
   ▼
Callees
```

也就是可以直接從某個 symbol 往上、往下探索：

- 誰呼叫它
- 它呼叫誰
- 對應 source code
- 相關 dependency

所以如果接手陌生專案，也可以自己拿它來探索，不一定只有 AI Agent 才能使用。

---

## 4. 實際可以怎麼用？

基本流程比想像中簡單。

Linux 安裝：

```bash
curl -fsSL https://raw.githubusercontent.com/colbymchenry/codegraph/main/install.sh | sh
```

接著：

```bash
codegraph install
```

它會偵測 Coding Agent，並協助把 CodeGraph MCP 接進去。

然後進入自己的專案：

```bash
cd report_implement
codegraph init
```

它會產生：

```text
.codegraph/
```

裡面就是 local index。

整體流程：

```text
安裝 CodeGraph
      ↓
連接 Coding Agent / MCP
      ↓
進入 Repository
      ↓
codegraph init
      ↓
建立 local code graph
      ↓
Codex / Claude Code 等 Agent 查詢 graph
```

目前 CodeGraph 也有 auto-sync 的設計：

```text
修改 code
     ↓
CodeGraph 偵測
     ↓
更新 graph
     ↓
Coding Agent 查到最新關係
```

因此不是每修改一次 code，都要手動重新執行完整的 `init`。

---

## 5. 一個很重要的點：100% Local

這點對工作環境尤其重要。

CodeGraph README 強調它的 code graph 是：

**100% local。**

也就是：

```text
Source Code
     ↓
local indexing
     ↓
.codegraph/
     ↓
local MCP
     ↓
Coding Agent
```

CodeGraph 本身不是：

```text
Source Code
↓
上傳 CodeGraph Cloud
↓
分析
```

所以如果拿公司 code 使用，至少在 CodeGraph 這一層，不需要為了建立 graph 把 source code 上傳到 CodeGraph 的服務。

但需要分清楚：

> **CodeGraph local，不代表整個 AI coding pipeline 都是 local。**

Codex、Claude Code 或其他 Coding Agent 本身如何處理程式碼，是另外一個獨立問題。

---

## 6. 它跟現在寫的專案文件會不會重疊？

目前可能會維護：

```text
AGENTS.md
00_map
04_phase1
設計決策
pipeline 說明
```

乍看可能會想：

> 「既然 CodeGraph 自己知道 code 關係，那我還寫這些幹嘛？」

其實兩者是**互補**，不是互相取代。

例如 CodeGraph 可以知道：

```text
build_report.py
      ↓
run.py
      ↓
gpu.py
```

它知道的是：

> **「現在 code 是什麼、怎麼連。」**

但是設計文件可能記錄：

> 原本考慮 A / B / C 三種方式，最後因為 X 原因選 B。未來如果需求 Y 出現，可以改成 C。

CodeGraph 並不知道這件事情。

因此 AI coding 環境可以變成：

```text
                 Codex
              /    |    \
             /     |     \
            ▼      ▼      ▼

       AGENTS.md  Docs   CodeGraph
           │       │        │
           ▼       ▼        ▼
        Rules   Decisions  Reality

       怎麼做    為何做    Code怎麼連
```

這樣其實比單純堆很多 Markdown 文件更健康。

### 人工文件保留

- 需求
- 規則
- 設計決策
- 為什麼這樣設計
- 限制
- 歷史背景
- 未來規劃

### CodeGraph 處理

- 誰 call 誰
- dependency
- symbol relationship
- cross-file relationship
- call path
- change impact
- 現在程式碼實際結構

也就是把「程式碼結構事實」盡量交給工具自動維護。

---

## 7. 哪些情況沒必要用？

它不是每個 repository 都需要。

如果專案只有：

```text
main.py
utils.py
config.py
```

總共大約 1,000 行 code，Codex 用 `grep + read` 很快就能理解。這種情況多一個 CodeGraph 反而不一定有明顯價值。

CodeGraph 的價值通常會隨著以下因素增加：

```text
檔案數量 ↑
module 數量 ↑
cross-file call ↑
dependency ↑
AI 修改頻率 ↑
多人維護 ↑
```

只有 10 files 可能沒有太大感覺；但到了 100+、500+、1000+ files，Agent 每次重新探索 codebase 的成本就會開始變得明顯。

因此比較適合：

- 中大型 repository
- 長期維護專案
- 模組很多的專案
- cross-file dependency 複雜的專案
- 常使用 AI Coding Agent 修改 code 的專案
- 接手陌生 codebase
- refactor 前需要 impact analysis

---

## 8. 對我的實際價值

我的判斷是：

> **很適合，可以實際試用。**

不是單純「先收藏」。

原因不是因為會 Python，也不是因為以前做 Kernel，而是現在的開發模式已經逐漸變成：

```text
我
 ↓
規劃 / Decision
 ↓
AGENTS.md + Docs
 ↓
Codex
 ↓
修改 Repository
 ↓
我 Review
```

CodeGraph 很自然可以插在這裡：

```text
我
 ↓
規劃
 ↓
AGENTS.md + Docs
 ↓
Codex
 ↕
CodeGraph
 ↓
Repository
```

尤其如果一直在思考：

> 「怎麼讓 AI 理解我的專案，又不要維護一大堆重複文件？」

CodeGraph 剛好可以把**「程式碼結構事實」**這部分從人工文件裡拿掉。

仍然由人維護需求、規則、設計決策、重要背景；至於誰 call 誰、dependency、symbol 關係、change impact，則交給 CodeGraph。

這個分工很適合目前 AI 協作開發的方式。

---

## 9. 建議怎麼試

先不用直接拿最大的工作專案測。

可以先拿目前已有一定結構、但又不至於太大的 report pipeline 做小實驗：

```text
① 原本 Codex
   ↓
問 3～5 個 codebase 問題

② 安裝 CodeGraph
   ↓
codegraph init

③ 再讓 Codex 做類似問題

④ 比較
   ├─ Codex tool calls
   ├─ 是否亂讀檔
   ├─ 理解 dependency 是否正確
   ├─ 修改前有沒有找到 impact
   └─ 整體速度
```

可以刻意測這幾類問題：

### Code navigation

> 這個 function 是從哪裡被呼叫的？

### Dependency

> GPU report 最後到 PDF 的完整流程是什麼？

### Impact analysis

> 如果修改這個 function，可能影響哪些 module？

### Refactor

> 我要把這段功能抽成共用 module，哪些 caller 需要一起改？

### Bug tracing

> 這個 value 從入口一路傳到這裡經過哪些 function？

如果使用 CodeGraph 後，Codex 明顯少讀很多無關檔案、比較快找到正確 dependency、修改前更容易找出 impact、大型任務比較不容易漏掉 caller，那就值得導入較大的工作專案。

反過來，如果目前專案規模下完全感覺不到差異，也不用為了「有 graph 很酷」硬增加一層工具。

---

## 10. 跟近期研究工具的定位差異

CodeGraph 跟 DSPy、SkillOpt 其實不是同一類工具。

### DSPy

比較偏：

> **程式化建立與最佳化 LLM pipeline。**

如果目前主要是在使用現成 Coding Agent，而不是自己開發複雜 LLM application，未必需要立刻導入。

### SkillOpt

比較偏：

> **最佳化 Agent Skill / instruction / workflow。**

適合之後開始大量建立自己的 Skill、Agent workflow 時研究。

### CodeGraph

比較偏：

> **直接改善 Coding Agent 對現有 repository 的理解能力。**

因此它跟目前的 Codex + Repository + AGENTS.md 工作流關係最直接。

```text
DSPy
→ 最佳化 LLM Program

SkillOpt
→ 最佳化 Skill / Agent 行為

CodeGraph
→ 最佳化 Agent 對 Codebase 的理解
```

所以就目前實際使用優先度來看，CodeGraph 是很適合近期直接安裝測試的一個工具。

---

## 11. 最後判斷

### 值不值得研究？

**很適合，可以實際使用。**

它不是那種需要先花很多時間研究理論才能知道有沒有用的工具。

最好的方式反而是：

> **直接找一個正在用 Codex 維護的 repository，裝起來跑一次。**

如果有效，它會直接改善目前已經存在的 AI coding workflow。

我最看重的不是單純：

> 「省多少 Token。」

而是：

> **讓 Agent 更快理解 repository、降低漏看 dependency 的機率，並在修改程式前更可靠地分析 impact。**

對現在的使用方式來說，這三點比單純節省 token 更有價值。

---

## 相關連結

- [CodeGraph GitHub](https://github.com/colbymchenry/codegraph)
