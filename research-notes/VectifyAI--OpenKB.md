# OpenKB

- Repository: https://github.com/VectifyAI/OpenKB
- 類型：開源知識庫 / Knowledge Compilation / RAG 替代方案 / Agent Skill 生成工具
- 適合：把 PDF、文件、網頁與技術資料長期整理成可查詢、可連結、可重複利用的 AI Wiki

## 1. 這是什麼？

OpenKB（Open Knowledge Base）是一套把原始文件「編譯」成結構化 Wiki 知識庫的開源系統。

它不是單純把文件切成 chunks、做 embedding，再放進 Vector DB。OpenKB 的核心想法是：讓 LLM 在資料加入知識庫時，就先把內容整理成可長期保存的知識，包括摘要、概念頁、實體頁與不同知識之間的交叉連結。之後新增文件時，既有概念頁也會被更新，因此知識會逐步累積，而不是每次問問題都重新從原始文件中找答案。

可以把它理解成：

```text
PDF / Word / PPT / Markdown / Excel / CSV / HTML / URL
                         ↓
                       OpenKB
                         ↓
              Knowledge Compilation
                         ↓
       ┌──────────────────────────────┐
       │ Summary pages                │
       │ Concept pages                │
       │ Entity pages                 │
       │ Cross-links                  │
       │ Sources / Images             │
       └──────────────────────────────┘
                         ↓
                  Markdown Wiki
                         ↓
       Query / Chat / Skill / Slides / Graph
```

因此它比較像「AI 幫你維護的個人知識庫編譯器」，而不是單純的 Chat with PDF。

## 2. 和傳統 RAG 最大差異

典型 RAG 大致是：

```text
文件
 ↓
切 chunk
 ↓
Embedding
 ↓
Vector DB
 ↓
每次問題重新搜尋
 ↓
LLM 回答
```

OpenKB 則是：

```text
文件
 ↓
理解與整理
 ↓
建立 Summary / Concept / Entity
 ↓
與既有知識交叉連結
 ↓
持久化 Wiki
 ↓
Query / Chat / Agent 使用
```

傳統 RAG 的知識主要留在原始 chunks 與索引中；OpenKB 則會額外建立一層「已整理過的知識」。

例如先加入一份 NUMA Performance Guide，OpenKB 可能建立：

- NUMA
- CPU Affinity
- Memory Locality

之後再加入 Linux Memory Optimization 文件，它可能更新原本的 NUMA、Memory Locality 頁面，並新增 HugePages 等概念。

也就是：

```text
Document A ─┐
            ├── NUMA
Document B ─┘
```

新的資料會豐富既有知識，而不是只多出另一批 chunks。

## 3. Knowledge Compilation

這是 OpenKB 最重要的設計。

加入文件時，LLM 會：

1. 產生文件 Summary。
2. 讀取既有 Concept 與 Entity pages。
3. 建立或更新 Concept pages。
4. 建立或更新人物、組織、地點、產品等 Entity pages。
5. 建立不同頁面之間的 Cross-links。
6. 更新 Knowledge Base index 與 log。

官方 README 提到，一份來源可能同時影響約 10～15 個 Wiki pages。

因此 Knowledge Base 會隨資料增加逐漸成熟。

## 4. 長文件：PageIndex

OpenKB 使用 VectifyAI 的 PageIndex 處理長 PDF。

它強調 vectorless、reasoning-based retrieval，不主要依賴 embedding similarity，而是先建立文件的階層式 Tree Index。

概念上類似：

```text
Document
│
├── Chapter 1
│   ├── Section 1.1
│   └── Section 1.2
├── Chapter 2
└── Chapter 3
```

當問題出現時，LLM 可以先判斷問題與哪個章節、節點相關，再進一步讀取內容。

這種方式特別適合：

- Technical manual
- Paper
- Specification
- 教科書
- 很長且結構明確的 PDF

預設 PDF 達 20 頁以上會走 PageIndex long-document pipeline；較短文件則直接轉成 Markdown 後讓 LLM 閱讀。

## 5. 支援的資料

目前支援：

- PDF
- Word
- Markdown
- PowerPoint
- HTML
- Excel
- CSV
- Text
- URL

短文件：

```text
文件 → MarkItDown → Markdown → LLM
```

長 PDF：

```text
PDF → PageIndex → Tree Index / Summary → LLM
```

圖片、表格與 figures 也能納入處理，而不是只處理純文字。

## 6. Query 與 Chat

建立 Knowledge Base 後，可以直接詢問：

```bash
openkb query "What are the main findings?"
```

Query 會根據 Wiki 與來源提供有引用依據的回答，也可以把結果保存到 `wiki/explorations/`。

如果需要持續討論：

```bash
openkb chat
```

Chat 支援 multi-turn session，並可以保存、恢復或刪除 session。

聊天中也能直接新增資料、建立 Skill、建立簡報、執行 lint 等操作。

## 7. Skill Factory

這是 OpenKB 對我特別有價值的功能之一。

它可以把整個 Knowledge Base 再蒸餾成可攜式 Agent Skill：

```text
大量 PDF / 文件 / 網頁
          ↓
      OpenKB Wiki
          ↓
      Skill Factory
          ↓
        SKILL.md
      + references/
```

例如：

```bash
openkb skill new linux-performance \
  "Reason about Linux server performance tuning"
```

會建立：

```text
output/skills/linux-performance/
├── SKILL.md
└── references/
```

這些 Skill 可以給 Claude Code、OpenAI Codex、Gemini CLI 等 Agent 使用。

它不是單純把文件摘要塞進 SKILL.md，而是嘗試整理成 decision rules、判斷方式、適用範圍與相關 reference，讓其他 Agent 能用這套知識進行推理。

### Skill 評估

OpenKB 還提供：

- `skill validate`：檢查 Skill 結構。
- `skill eval`：測試 Skill 是否在正確的問題觸發，以及內容是否足以支撐宣稱的能力。
- `skill history`：查看歷史版本。
- `skill rollback`：回復先前版本。

因此它已經不只是 Skill generator，而有點像一套 Skill development pipeline。

## 8. 和 book-to-skill 的差別

兩者有交集，但層級不同。

book-to-skill 比較像：

```text
一本書 / 一份主要材料
          ↓
        Skill
```

OpenKB 比較像：

```text
很多 PDF / 網頁 / 文件
          ↓
    Knowledge Base
          ↓
        Skill
```

所以 book-to-skill 很適合「把一本書變成可使用的 Skill」，OpenKB 則更適合「把整個領域的資料累積成知識庫，再從知識庫產生領域型 Skill」。

兩者不一定互斥。

## 9. Obsidian

OpenKB 產生的 Wiki 是普通 Markdown 檔案，使用 `[[wikilinks]]` 建立頁面關係，因此可以直接把 `wiki/` 當成 Obsidian Vault 開啟。

可以在 Obsidian 裡：

- 閱讀 Summary。
- 瀏覽 Concepts。
- 查看 Entities。
- 查看不同知識之間的 backlinks。
- 使用 Graph View 看知識關係。

這代表 OpenKB 不會把知識鎖在自己的資料庫格式裡，Markdown 本身仍然可以人工閱讀與修改。

## 10. Knowledge Workbench Web UI

OpenKB 不只提供 CLI，也附帶 Web UI。

安裝：

```bash
pip install "openkb[web]"
```

啟動：

```bash
openkb-web
```

預設可以從：

```text
http://127.0.0.1:7566/
```

開啟 Knowledge Workbench。

Web UI 可以：

- 瀏覽 Knowledge Base。
- 上傳與 Compile 文件。
- Query。
- Chat。

所以不一定要全程透過 CLI 操作。

## 11. Knowledge Graph

執行：

```bash
openkb visualize
```

可以產生：

```text
output/visualize/graph.html
```

提供 3D、mind-map、radial 等知識圖瀏覽方式。

我會把這個功能視為方便理解知識結構的視覺介面，而不是 OpenKB 最主要的核心價值。

## 12. Slides

Knowledge Base 還能直接產生 HTML slide deck：

```bash
openkb deck new my-deck "An intro deck on NUMA optimization"
```

所以整體可以理解為：

```text
                    ┌── Query
                    ├── Chat
文件 → OpenKB Wiki ─┼── Skill
                    ├── Slides
                    └── Knowledge Graph
```

Wiki 是底層知識，Query、Chat、Skill、Slides 等都是建立在上面的 generators。

## 13. LLM 支援

OpenKB 透過 LiteLLM 支援多種 Provider，例如：

- OpenAI
- Anthropic Claude
- Gemini
- OpenRouter
- Ollama
- LM Studio
- llama.cpp
- GitHub Copilot
- Amazon Bedrock

OAuth 類 Provider，例如 `chatgpt/*`、`github_copilot/*`，可以不使用額外 API Key。

Local model 也能使用，但大型文件的 Knowledge Compilation 對模型理解與推理能力要求不低，小型本地模型的整理品質可能與較強的雲端模型有差距。

## 14. 基本使用流程

安裝：

```bash
pip install openkb
```

建立 Knowledge Base：

```bash
mkdir my-kb
cd my-kb
openkb init
```

加入文件：

```bash
openkb add paper.pdf
```

加入整個資料夾：

```bash
openkb add ~/papers/
```

加入 URL：

```bash
openkb add https://example.com/article
```

詢問：

```bash
openkb query "這些文件對 NUMA tuning 有什麼建議？"
```

互動聊天：

```bash
openkb chat
```

如果想要 GUI，再啟動 Knowledge Workbench。

## 15. 對我的實際用途

### Server / Linux 技術知識庫

這是目前最值得嘗試的方向。

可以建立：

```text
server-kb/
```

逐步加入：

- SPEC CPU2017 文件
- Intel optimization guide
- AMD MI300X 文件
- RCCL 文件
- NUMA / Linux Memory 文件
- MLPerf 文件
- Networking / NIC 文件
- 自己整理的 Markdown debug 筆記
- Benchmark report
- Grafana / Server debug SOP

最後可能形成：

```text
Server KB
│
├── CPU Performance
├── NUMA
│   ├── taskset
│   ├── numactl
│   ├── memory locality
│   └── THP
├── Memory
├── GPU
│   ├── MI300X
│   └── RCCL
├── MLPerf
├── Networking
└── Benchmark Debugging
```

之後就可以問：

- 哪些文件提過 NUMA interleave 對 benchmark 的影響？
- THP always / never 可能影響哪些 workload？
- MI300X RCCL bandwidth 問題應該優先檢查什麼？
- 過去整理的 Server performance debugging 方法有哪些？

這比每次重新把文件交給 AI 更適合長期累積工作知識。

### 建立 Server Performance Agent Skill

累積足夠資料後，可以進一步：

```text
Server KB
    ↓
Skill Factory
    ↓
server-performance-engineer
```

讓 Codex、Claude Code 或 Gemini CLI 在處理相關工作時使用這套領域知識。

這可能比單純建立一個很長的 prompt 更容易維護，也能隨 Knowledge Base 更新。

### GitHub / AI 工具研究知識庫

另一種可能是把研究過的 GitHub AI 工具、README、比較筆記整理進另一個 KB。

但目前我會優先把 OpenKB 用在「工作技術知識」這種高價值、會長期累積、不同文件彼此有關聯的內容，而不是一開始就把所有生活與收藏資料全部丟進去。

## 16. 和其他工具的定位

| 工具 | 主要用途 |
| --- | --- |
| PageIndex | 長文件 Tree Index 與 reasoning-based retrieval |
| Obsidian LLM Wiki | 在 Obsidian 中建立 AI Wiki 與知識連結 |
| book-to-skill | 將書籍 / 文件轉成 Agent Skill |
| 傳統 RAG | 文件索引、檢索，再回答問題 |
| OpenKB | 多來源資料 → 持久 Wiki → Query / Chat / Skill / Slides |

PageIndex 是 OpenKB 使用的底層長文件 retrieval 能力之一；OpenKB 則是完整 Knowledge System。

## 17. 目前限制

OpenKB 還不是成熟的大型企業 Knowledge Platform。

目前 Roadmap 仍包括：

- 將 long-document handling 擴展到非 PDF 格式。
- 大型 document collection 的 nested folder support。
- Massive Knowledge Base 的 hierarchical concept indexing。
- Database-backed storage engine。

所以如果目標是管理數萬、數十萬份企業文件，目前不一定是最適合的選擇。

現階段更適合：

- 個人 Knowledge Base。
- 技術研究資料。
- 數十到數百份高價值文件。
- Paper / Manual / Specification。
- 想把知識進一步提供給 AI Agent 使用的人。

## 18. 值不值得研究？

**很適合我，可以實際使用。**

原因不是它又提供了一套 RAG，而是它把幾個我正在關注的方向串在一起：

```text
文件 / Paper / 技術資料
          ↓
      AI 自動整理
          ↓
       Markdown Wiki
          ↓
     持續累積知識
          ↓
 Query / Chat / Obsidian
          ↓
       Agent Skill
```

對目前需求來說，最值得測試的不是建立「所有資料的第二大腦」，而是先做一個範圍清楚的 **Server Performance Knowledge Base**。

如果實際測試後發現：

1. 技術文件整理品質夠好。
2. Concept pages 不會過度重複。
3. 新文件真的能有效更新舊知識。
4. Query 能準確回到來源。
5. Skill Factory 產生的 Skill 對實際 Server debugging 有幫助。

那它就很有機會成為長期使用的知識整理工具。

## 19. 最適合我的第一個實驗

不要一開始丟幾百份資料。

可以先挑約 5～10 份彼此高度相關的 Server Performance 文件，例如 NUMA、THP、CPU affinity、SPEC CPU 等資料，建立第一個 KB。

觀察：

- 自動產生哪些 Concept。
- 不同文件是否真的被整合。
- Wiki 在 Obsidian 裡是否好閱讀。
- Query 的引用是否可靠。
- 加入第 6、7 份文件後，既有 Concept 是否合理更新。
- 最後產生一個 `server-performance` Skill，實際交給 Agent 解幾個過去遇過的問題。

如果這個小型測試有效，再逐步擴充 MI300X、RCCL、MLPerf、Networking 等領域。

---

## 參考

- OpenKB Repository: https://github.com/VectifyAI/OpenKB
- PageIndex: https://github.com/VectifyAI/PageIndex
