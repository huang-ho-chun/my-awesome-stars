# RRSI｜GitHub 專案導覽

> 來源：[google-research/rrsi](https://github.com/google-research/rrsi) 專案 README；查閱日期：2026-09-29。

## 1. 這是什麼？

**RRSI（Regularized Recursive Self-Improvement of Agent Harnesses）** 是 Google Research 公開的 AI Agent 自我改進研究框架。

最簡單的理解是：

> **讓 AI Agent 自己反覆修改「包在模型外面的整套工作方式」，再用實際 Benchmark 決定哪些修改值得留下。**

它不是重新訓練 Claude、Gemini、GPT 這類基礎模型，而是固定模型本身，改良模型外圍的 **Agent harness**。

Harness 可以包含：

- System Prompt / 工作指引
- Control flow / 任務流程
- Tools
- Skills
- Memory
- Context management
- Configuration
- Sub-agents

因此 RRSI 不只是 Prompt Optimizer，而比較像是 **AI Agent 的自動化 A/B Testing + Agent Workflow / Harness Optimizer**。

概念流程如下：

```text
目前 Agent
   ↓
分析失敗案例與目前表現
   ↓
提出改善假設
   ↓
產生候選版本 A / B
   ↓
檢查候選是否有 Benchmark-specific 偷吃步
   ↓
執行 Benchmark
   ↓
比較品質、成本與測量誤差
   ↓
接受較好的候選
   ↓
記錄這次修改與結果
   ↓
進入下一輪
```

如果一般 Prompt Optimization 是「幫我找更好的 Prompt」，RRSI 更接近：

> **幫我找更好的 Agent 設計。**

---

## 2. 它解決什麼問題？

Agent 的能力不只取決於模型本身。

即使固定同一個 LLM：

```text
LLM
 ↓
System Prompt
 ↓
Planning / Control Flow
 ↓
Tools
 ↓
Skills
 ↓
Memory
 ↓
Context Management
 ↓
Sub-agent
```

上面這些設計不同，最後的任務成功率可能差很多。

因此一個自然想法是：

> 既然 Agent 可以寫程式、修改 Prompt、建立 Tool，能不能讓 Agent 自己修改自己的 Harness？

可以，但會遇到一個很大的問題：**Overfitting。**

如果一直針對固定 Benchmark 演化，Agent 可能不是學到更好的通用工作方法，而是逐漸記住測試集的特徵，例如加入只對某幾個 Task 有效的特殊規則。

RRSI 的核心研究問題就是：

> 如何讓 Harness 可以自由演化，同時降低它對 evolve set 過度擬合的風險？

這也是名稱裡 **Regularized** 的來源。

---

## 3. RRSI 怎麼避免 Agent 越改越偏？

### 3.1 限制每一輪一次修改太多東西

RRSI 使用 annealed edit budget，限制單一候選版本可以同時包含多少獨立修改。

例如避免一次：

```text
改 Prompt
+ 改 Memory
+ 新增 Tool
+ 改 Planner
+ 新增 Sub-agent
```

如果一次全部修改，即使分數上升，也很難知道到底是哪一項有效。

因此 RRSI 會控制搜尋過程，而不是直接限制 Harness 最終能包含哪些元件。

### 3.2 記住以前試過的假設

每次修改都會留下 edit history，包括：

- 修改哪個 component
- 改善假設（hypothesis）
- Score 變化
- Cost 變化
- 是否被接受

Proposer 下一輪會看到完整歷史。

如果某個假設已經被實驗否定，就降低重複提出同一個想法的機會。

這讓整個演化比較像有實驗紀錄的工程迭代，而不是每輪重新猜。

### 3.3 卡住時強迫探索沒試過的方向

如果連續幾輪沒有改善，RRSI 會偵測 stalled run，並把 proposer 導向尚未充分探索的 component。

例如一直修改 Prompt 都沒有改善，就可能轉向：

- Tool
- Skill
- Memory
- Sub-agent
- Context management

避免搜尋一直困在同一種修改方式。

### 3.4 Critic 先檢查 Benchmark leakage

每個 Candidate 在真正跑 Benchmark 前會先經過 Critic。

目的之一是攔截 suite-specific logic，例如針對特定 Task ID、Benchmark 格式或測試資料寫死特殊處理。

因此它不是單純「分數高就接受」。

### 3.5 改善必須超過 Benchmark 的雜訊

假設：

```text
舊版：80.1
新版：80.3
Benchmark variance：±0.5
```

這種 +0.2 很可能只是測量誤差。

RRSI 使用 noise-adjusted floor / delta，要求改善具有足夠證據，避免把隨機波動誤認為進步。

### 3.6 Token / inference cost 也算成本

Agent 很容易透過：

- 更長 reasoning
- 更多 Tool Calls
- 更多 Sub-agent
- 更多 Context

硬把 Benchmark 分數提高。

因此 RRSI 還會比較推論成本。

如果只增加很小的品質，但 Token 成本大幅增加，候選不一定會被接受。

### 3.7 沒有持續貢獻的元件可以被移除

RRSI 不只是一直增加新東西。

History 也會建立 prune set，把已經不再帶來幫助的 machinery 交給 proposer 移除。

因此演化方向不是：

```text
Agent
→ 越來越複雜
→ 越來越貴
```

而是嘗試維持「改善效果值得增加的複雜度」。

---

## 4. 它目前拿什麼做實驗？

官方提供三個 Domain。

### Coding Agent

主要使用：

- Terminal-Bench 2.1：作為 evolve set
- SWE-bench Verified：作為 out-of-distribution 評估

README 公布的結果：

| Benchmark | Base Harness | RRSI | 差異 |
|---|---:|---:|---:|
| Terminal-Bench 2.1 | 74.2 | 80.2 | +6.0 |
| SWE-bench Verified | 82.0 | 83.8 | +1.8 |

這個實驗的重要點不只是 Terminal-Bench 上升，而是沒有直接參與 Harness 搜尋的 SWE-bench Verified 也有改善，用來檢查改善是否具有一定泛化能力。

### Agentic Workspace

主要使用：

- Harvey LAB
- JobBench
- GDPval
- APEX-Agents

README 結果：

| Benchmark | Base Harness | RRSI | 差異 |
|---|---:|---:|---:|
| Harvey LAB evolve | 89.4 | 90.5 | +1.1 |
| Harvey LAB held-out | 86.9 | 89.2 | +2.3 |
| JobBench | 36.0 | 40.7 | +4.7 |
| GDPval | 48.8 | 52.3 | +3.5 |
| APEX-Agents | 34.2 | 37.9 | +3.7 |

這一類比較接近企業知識工作、文件處理與工具使用 Agent。

### Engineering Design

使用：

- EngDesign
- EngDesign v1
- Frontier-Eng

README 結果：

| Benchmark | Base Harness | RRSI | 差異 |
|---|---:|---:|---:|
| EngDesign evolve | 50.0 | 54.9 | +4.9 |
| Frontier-Eng | 17.7 | 22.0 | +4.3 |

因此同一套 RRSI loop 並不是只為 Coding Agent 設計，而是透過 Domain adapter 套到不同類型的 Agent。

---

## 5. Git Worktree 的設計很值得注意

RRSI 每個候選 Harness 都會建立在獨立的 Git Worktree。

概念上像：

```text
目前版本 H_t
├── Candidate A
└── Candidate B
```

兩個 Candidate 都：

1. 從目前 incumbent 建立。
2. 各自修改 Harness。
3. 經過 Critic。
4. 執行 Benchmark。
5. 比較結果。

如果 A 勝出，`evolve/<domain>` branch 就 fast-forward 到 A。

因此 incumbent 永遠是一個 Git commit。

這讓整個 Agent 演化歷史可以被稽核：

```text
v1
 ↓
v2
 ↓
v3
 ↓
v4
```

可以回頭確認：

- 哪一輪改了什麼
- 為什麼修改
- Score 增加多少
- Token / Cost 增加多少
- 哪些假設失敗
- 哪些元件後來被 prune

這對真正做 Agent Engineering 很有價值。

---

## 6. 對我有什麼用？

對我來說，RRSI 最值得研究的地方不是「現在把它安裝起來」，而是理解：

> **未來可以怎麼自動優化我自己的 Agent / Skill / 工作流程。**

我平常已經會研究與使用：

- Agent Skills
- Codex / Coding Agent
- DSPy
- GEPA
- SkillOpt
- book-to-skill
- Planning with Files

RRSI 可以看成這條路線更上一層的工具。

粗略比較：

| 工具 | 主要優化對象 |
|---|---|
| DSPy | Prompt / LM Program |
| GEPA | Prompt、文字參數與 Agent behavior |
| SkillOpt | Agent Skill |
| RRSI | 整個 Agent Harness |

RRSI 的 Search Space 更大，可以碰：

```text
Prompt
Tool
Skill
Memory
Control Flow
Context
Configuration
Sub-agent
```

因此它的潛力比較大，但實驗成本與導入難度也明顯更高。

---

## 7. 我可能真的用得到的情境

### 情境一：Linux / Server Debug Agent

例如建立自己的：

```text
Linux Debug Agent
```

專門處理：

- dmesg / system log
- Network
- NUMA
- Docker
- GPU / RCCL
- Performance
- Grafana
- Kernel / Driver

第一版可能只是：

```text
1. 收集錯誤資訊
2. 找關鍵 log
3. 建立 root-cause hypothesis
4. 提供驗證 command
5. 根據結果繼續縮小範圍
```

之後把過去遇過的 50～200 個案例整理成 Benchmark。

RRSI 就可以嘗試探索：

- 修改 debug workflow
- 增加 log summarizer
- 加 hypothesis ranking
- 加 command verification
- 改 Context 管理
- 新增 Tool
- 新增 Memory
- 拆成不同 Sub-agent

然後用真實案例測：

```text
Linux Debug Agent v1
        ↓
Benchmark
        ↓
RRSI
        ↓
Linux Debug Agent v2
```

這比單純人工一直修改 Prompt 更接近系統化 Agent Engineering。

### 情境二：GitHub Project Research Agent

也可以把目前「閱讀 GitHub Repository → 判斷這是什麼 → 對我有沒有用 → 使用情境 → 怎麼開始 → 值不值得研究」這套流程做成 Agent。

準備一批以前研究過的 Repository，再定義評分方式，例如：

- 有沒有抓到核心用途
- 是否避免過度深入原始碼
- 是否提供實際使用情境
- 是否正確判斷導入成本
- 是否能針對使用者背景給出有意義的用途
- 是否能區分「值得收藏」與「現在值得實際導入」

之後就能測試不同 Prompt、Skill、Tool 與流程設計。

### 情境三：Server Performance Agent

把 SPEC CPU、NUMA、GPU、RCCL、MLPerf 等實際工作案例累積成 Dataset。

Agent 不只是回答問題，而是：

```text
讀取測試結果
→ 找異常
→ 建立假設
→ 建議下一個測試
→ 比較前後結果
→ 更新判斷
```

這種有明確輸入、流程與驗證結果的任務，比純聊天更適合做 Harness Optimization。

---

## 8. 我要怎麼用？

如果只是想理解 RRSI，目前不用急著安裝。

真的要開始使用，大致流程是：

```text
① 準備一個 Agent Harness
② 準備 Benchmark / Task Dataset
③ 定義 Domain Adapter
④ 定義執行與 Score 方法
⑤ 設定可演化的 Harness
⑥ 跑 Baseline
⑦ 讓 RRSI 產生 Candidate
⑧ 跑 Benchmark
⑨ Selection 選 Winner
⑩ 重複多輪
```

### 基本安裝

官方要求 Python 3.10+：

```bash
git clone https://github.com/google-research/rrsi.git
cd rrsi
pip install -e ".[dev]"
python3 -m pytest tests
```

### LLM 設定

官方實驗使用 Vertex AI。

README 發布版本使用 Claude Opus 4.8 作為 proposer、analyst、critic 與 frozen policy；其他實例也會使用 Gemini 作 Judge。

程式接受 LiteLLM model string，因此方法本身不是綁死單一模型家族。

### 執行 Domain

基本形式：

```bash
python3 rrsi.py --domain <coding|workspace|eng> smoke
python3 rrsi.py --domain <name> baseline
python3 rrsi.py --domain <name> run
python3 rrsi.py --domain <name> status
```

其中：

- `smoke`：先確認環境與 Candidate 可以正常執行。
- `baseline`：測目前 Harness H0。
- `run`：開始多輪演化。
- `status`：查看目前進度。

每一輪預設會建立兩個 Candidate，在獨立 Git Worktree 修改、檢查、測試，再把勝出的版本變成新的 incumbent。

---

## 9. 如果要加入自己的 Domain

RRSI 並不是只能跑官方三個 Benchmark。

自己的 Domain 主要要提供：

- evolve tasks
- held-out tasks
- smoke tasks
- Agent 執行方法
- Score 方法
- Trial / Trace 的讀取方式
- Candidate smoke test
- Critic patterns
- Component signals
- Guards
- Harness path
- Skill / Pattern 指引
- Hyperparameters

也就是說真正困難的地方通常不是：

> 「怎麼把 RRSI 跑起來？」

而是：

> **「怎麼定義一個可信的 Benchmark，讓 RRSI 知道什麼叫真的變好？」**

---

## 10. 最大限制：成本很高

RRSI 不是：

```bash
pip install rrsi
rrsi optimize
```

跑一下就完成。

假設：

```text
100 tasks
每個 task 平均 30k tokens
每輪 2 個 candidates
```

光 Candidate evaluation 就可能是：

```text
100 × 30k × 2
= 6,000,000 tokens / round
```

而且還沒有算：

- Proposer
- Analyst
- Critic
- 重複 trial
- Baseline
- Held-out evaluation
- 多輪演化

因此這比較像 **Agent Research / Agent Engineering Framework**，不是一般個人使用者裝完就能獲得效益的工具。

如果沒有穩定 Benchmark，花大量 Token 也不一定能得到真正有意義的改善。

---

## 11. 跟我最近研究的工具怎麼串起來？

可以把幾個專案理解成：

```text
book-to-skill
      ↓
從資料建立 Skill

SkillOpt / GEPA
      ↓
改善 Skill / Prompt

RRSI
      ↓
改善整個 Agent Harness
```

另一個角度是：

```text
以前：

人
↓
設計 Agent
↓
測試
↓
人工修改


RRSI 想做：

人
↓
定義 Task + Benchmark + Guardrails
↓
AI 提出 Harness 修改
↓
自動測試
↓
自動選擇
↓
反覆演化
```

因此人的角色逐漸從：

> 「每一個 Prompt 要怎麼寫？」

轉成：

> **「我要怎麼定義什麼叫真正的好 Agent？」**

這是 RRSI 最值得理解的觀念。

---

## 12. 值不值得研究？

### 結論：有特定情境才有用，但非常值得收藏與理解

**目前不建議直接拿 RRSI 當日常工具。**

原因是：

- 需要自己有 Agent Harness。
- 需要 Task Dataset / Benchmark。
- 需要可信的評分方式。
- 需要大量 LLM API / Token。
- 需要 Python、Git、Benchmark execution environment。
- Search Space 比 Skill / Prompt Optimization 大很多。

但如果未來已經建立：

- Linux Debug Skill / Agent
- Server Performance Agent
- GitHub Project Research Agent
- 英文學習 Agent
- 其他會重複使用的專業 Agent

並且累積 **50～200 個可重跑、可評分的真實案例**，RRSI 就會從「研究概念」變成非常值得實驗的工具。

對目前階段最值得帶走的不是安裝指令，而是這個思路：

> **先累積可重現的任務與評分方式；當 Benchmark 成熟之後，才有資格談自動化 Agent 改進。**

因此 RRSI 很適合放在 Agent / Skill Optimization 工具鏈的後段，作為未來從「使用 Agent」進一步走向「系統化 Agent Engineering」時再深入研究的專案。
