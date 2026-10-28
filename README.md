# 🌟 My Awesome Stars Collection

個人精選 GitHub Stars，按分類整理。涵蓋 AI Agent、LLM、數據可視化、知識管理、開發工具等多個領域。

**最後更新**：2026-10-28

---

## 📑 Table of Contents

- [🤖 AI Agent & 大模型](#-ai-agent--大模型)
- [📚 學習資源與教程](#-學習資源與教程)
- [🎨 設計與可視化工具](#-設計與可視化工具)
- [🔍 RAG & 知識管理](#-rag--知識管理)
- [💻 開發工具與效率](#-開發工具與效率)
- [🎬 視頻/音頻/內容生成](#-視頻音頻內容生成)
- [💰 金融與投資](#-金融與投資)
- [📖 資源合集](#-資源合集)
- [🔧 其他實用工具](#-其他實用工具)

---

## 🤖 AI Agent & 大模型

### 框架/引擎
- **[3dcodeverse](https://github.com/gaoypeng/3dcodeverse)** - 提供讓 Agent 以規劃、執行與視覺回饋製作 3D 資產的研究框架與資料集。 (⭐ 251)
  - [詳細說明](research-notes/gaoypeng--3dcodeverse.md)
- **[Harness²](https://github.com/google-research/harness2)** - 讓固定模型的 Agent 在任務中試改 Prompt、工具與 Skill 等 Harness 元件，並依執行證據保留改進。 (⭐ 7,151)
  - [詳細說明](research-notes/google-research--harness2.md)
- **[Langflow](https://github.com/langflow-ai/langflow)** - 用圖形介面串接模型、資料與工具，建立可部署的 AI Agent 工作流程。 (⭐ 154,880)
  - [詳細說明](research-notes/langflow-ai--langflow.md)
- **[DSPy](https://github.com/stanfordnlp/dspy)** - 以 Python 定義並評估 LLM 流程，再最佳化提示與模型設定。 (⭐ 38,065)
  - [詳細說明](research-notes/stanfordnlp--dspy.md)
- **[SkillOpt](https://github.com/microsoft/SkillOpt)** - 以任務驗證結果改善 Agent Skill 指引的工具與研究框架。 (⭐ 17,154)
  - [詳細說明](research-notes/microsoft--SkillOpt.md)
- **[RRSI](https://github.com/google-research/rrsi)** - 讓固定 LLM 的 Agent Harness 透過 Benchmark 反覆修改 Prompt、流程、工具、Skill、Memory 與 Sub-agent，並用正則化機制降低過度擬合。 (⭐ 846)
  - [詳細說明](research-notes/google-research--rrsi.md)
- **[OpenMAIC](https://github.com/THU-MAIC/OpenMAIC)** - 將主題或資料變成多 Agent 互動課堂的課程生成系統。 (⭐ 37,318)
  - [詳細說明](research-notes/THU-MAIC--OpenMAIC.md)
- **[Hermes Agent](https://github.com/NousResearch/hermes-agent)** - 整合工具、記憶與排程，可在終端或訊息平台使用的個人 Agent。 (⭐ 246,062)
  - [詳細說明](research-notes/NousResearch--hermes-agent.md)
- **[Hermes Desktop](https://github.com/fathah/hermes-desktop)** - 管理 Hermes Agent 聊天、設定與工作紀錄的社群桌面介面。 (⭐ 14,231)
  - [詳細說明](research-notes/fathah--hermes-desktop.md)

### Agent 工具
- **[Agency Agents](https://github.com/msitarzewski/agency-agents)** - 收錄工程、設計、研究等專職 AI Agent 指引，可挑選角色安裝到 Codex 等工具或當範本參考。 (⭐ 161,239)
  - [詳細說明](research-notes/msitarzewski--agency-agents.md)
- **[context-mode](https://github.com/mksglu/context-mode)** - 縮減 Coding Agent 工具輸出占用的上下文，保留可查詢內容。 (⭐ 23,185)
  - [詳細說明](research-notes/mksglu--context-mode.md)
- **[codex-skill-dashboard](https://github.com/tonywei49/codex-skill-dashboard)** - 在本機查看 Codex Skills 啟用狀態與使用紀錄，並管理暫停、說明翻譯和統計。 (⭐ 4)
  - [詳細說明](research-notes/tonywei49--codex-skill-dashboard.md)
- **[i-have-adhd](https://github.com/ayghri/i-have-adhd)** - 讓 Coding Agent 先說重點與下一步的輸出風格 Skill。 (⭐ 46,685)
  - [詳細說明](research-notes/ayghri--i-have-adhd.md)
- **[GitNexus](https://github.com/abhigyanpatwari/GitNexus)** - 為程式庫建立關係索引，查詢符號、呼叫路徑與修改影響。 (⭐ 47,380)
  - [詳細說明](research-notes/abhigyanpatwari--GitNexus.md)
- **[Agent-Reach](https://github.com/Panniantong/Agent-Reach)** - 替 Agent 設定並檢查多平台網路資料存取能力。 (⭐ 82,337)
  - [詳細說明](research-notes/Panniantong--Agent-Reach.md)
- **[OpenCLI](https://github.com/jackwener/OpenCLI)** - 將網站操作包成 Agent 可呼叫的命令，並可透過瀏覽器橋接沿用既有登入狀態。 (⭐ 29,595)
  - [詳細說明](research-notes/jackwener--OpenCLI.md)
- **[codegraph](https://github.com/colbymchenry/codegraph)** - 建立程式碼呼叫與相依關係索引，供 Coding Agent 查詢。 (⭐ 71,127)
  - [詳細說明](research-notes/colbymchenry--codegraph.md)
- **[context-hub](https://github.com/andrewyng/context-hub)** - 提供 Coding Agent 可查閱、可註記的版本化 API 文件。 (⭐ 13,981)
  - [詳細說明](research-notes/andrewyng--context-hub.md)

- **[SimpleMem](https://github.com/aiming-lab/SimpleMem)** - 為 LLM Agent 提供文字與多模態長期記憶、壓縮及檢索的研究與工具。 (⭐ 3,815)
  - [詳細說明](research-notes/aiming-lab--SimpleMem.md)

### 多模態
- **[JoyAI-Image](https://github.com/jd-opensource/JoyAI-Image)** - 整合圖片理解、文字生圖與指令式修圖的多模態模型專案。 (⭐ 2,220)
  - [詳細說明](research-notes/jd-opensource--JoyAI-Image.md)
- **[CosyVoice](https://github.com/QwenAudio/CosyVoice)** - 提供多語言語音生成與參考聲音複製的模型專案。 (⭐ 23,641)
  - [詳細說明](research-notes/QwenAudio--CosyVoice.md)
- **[Seedance 2.0](https://github.com/Emily2040/seedance-2.0)** - 規劃影片分鏡與參考素材的 Agent Skill，生成需外部服務。 (⭐ 7,342)
  - [詳細說明](research-notes/Emily2040--seedance-2.0.md)
- **[claude-video](https://github.com/bradautomates/claude-video)** - 讓 Coding Agent 結合字幕與影格分析影片內容的 Skill。 (⭐ 17,268)
  - [詳細說明](research-notes/bradautomates--claude-video.md)
- **[book-to-skill](https://github.com/virgiliojr94/book-to-skill)** - 將書籍與文件整理成可按需查閱的 Agent Skill。 (⭐ 30,879)
  - [詳細說明](research-notes/virgiliojr94--book-to-skill.md)
- **[VoxCPM](https://github.com/OpenBMB/VoxCPM)** - 支援多語言朗讀、聲音設計與參考聲音複製的語音模型。 (⭐ 37,639)
  - [詳細說明](research-notes/OpenBMB--VoxCPM.md)
- **[VibeVoice](https://github.com/microsoft/VibeVoice)** - 涵蓋長音訊辨識、多人語音與串流合成的語音 AI 專案。 (⭐ 54,336)
  - [詳細說明](research-notes/microsoft--VibeVoice.md)

### Agent Skills
- **[Elephant-Goldfish Model](https://github.com/google/elephant-goldfish-model)** - 以深度專案脈絡起草規格，並交由全新脈絡 Agent 審查盲點的設計 Skills。 (⭐ 3,521)
  - [詳細說明](research-notes/google--elephant-goldfish-model.md)
- **[Project Scaffold](https://github.com/kenming/project-scaffold-skill)** - 預覽並調整 Agent 規範與專案文件骨架，確認後才建立檔案。 (⭐ 14)
  - [詳細說明](research-notes/kenming--project-scaffold-skill.md)
- **[archify](https://github.com/tt-a1i/archify)** - 將程式碼或系統描述轉成可檢查的互動架構圖。 (⭐ 64,422)
  - [詳細說明](research-notes/tt-a1i--archify.md)
- **[diagram-design](https://github.com/cathrynlavery/diagram-design)** - 提供多種圖解類型與視覺規則的 Agent Skill。 (⭐ 40,413)
  - [詳細說明](research-notes/cathrynlavery--diagram-design.md)
- **[effective-html](https://github.com/plannotator/effective-html)** - 引導 Coding Agent 製作 HTML 圖解、線框圖與互動原型。 (⭐ 3,190)
  - [詳細說明](research-notes/plannotator--effective-html.md)
- **[flint-chart](https://github.com/microsoft/flint-chart)** - 讓 Agent 描述資料意義與圖表需求，再產生可讀圖表。 (⭐ 4,215)
  - [詳細說明](research-notes/microsoft--flint-chart.md)
- **[cangjie-skill](https://github.com/kangarooking/cangjie-skill)** - 從書籍、影片與播客萃取方法，轉成可呼叫的 Agent Skills。 (⭐ 10,145)
  - [詳細說明](research-notes/kangarooking--cangjie-skill.md)
- **[learn-from-materials](https://github.com/dmoshehun-prog/learn-from-materials)** - 將書籍、PDF、簡報與網頁整理成可追溯知識庫、互動學習頁及同步 Markdown 的 Agent Skill。 (⭐ 306)
  - [詳細說明](research-notes/dmoshehun-prog--learn-from-materials.md)
- **[ljg-skills](https://github.com/lijigang/ljg-skills)** - 涵蓋閱讀、學習、寫作、圖卡與思考分析的中文 Agent Skills 集合。 (⭐ 7,394)
  - [詳細說明](research-notes/lijigang--ljg-skills.md)
- **[dashi-ppt-skill](https://github.com/chuspeeism/dashi-ppt-skill)** - 讓 Agent 產生可在瀏覽器編輯、可輸出 PPTX 的簡報。 (⭐ 8,302)
  - [詳細說明](research-notes/chuspeeism--dashi-ppt-skill.md)
- **[holo-card-studio](https://github.com/EverettFish/holo-card-studio)** - 用 Codex Skill 製作全息卡牌、Blender 工程與互動頁面。 (⭐ 1,558)
  - [詳細說明](research-notes/EverettFish--holo-card-studio.md)
- **[skills](https://github.com/emilkowalski/skills)** - 協助 Coding Agent 改善介面設計、動畫與互動細節的 Skills。 (⭐ 38,203)
  - [詳細說明](research-notes/emilkowalski--skills.md)
- **[mattpocock/skills](https://github.com/mattpocock/skills)** - 涵蓋開發、除錯與規劃流程的 Agent Skills 集合。 (⭐ 263,348)
  - [詳細說明](research-notes/mattpocock--skills.md)
- **[andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills)** - 針對 Coding Agent 常見失誤整理的工作指引。 (⭐ 213,337)
  - [詳細說明](research-notes/multica-ai--andrej-karpathy-skills.md)
- **[last30days-skill](https://github.com/mvanhorn/last30days-skill)** - 蒐集多個來源近 30 天資訊並整理成研究摘要的 Skill。 (⭐ 62,129)
  - [詳細說明](research-notes/mvanhorn--last30days-skill.md)
- **[last30days-skill-cn](https://github.com/Jesseovo/last30days-skill-cn)** - 針對中文網路平台蒐集近 30 天資訊的研究 Skill。 (⭐ 1,793)
  - [詳細說明](research-notes/Jesseovo--last30days-skill-cn.md)
- **[yao-meta-skill](https://github.com/yaojingang/yao-meta-skill)** - 協助建立、檢查與更新其他 Agent Skills 的元技能。 (⭐ 2,617)
  - [詳細說明](research-notes/yaojingang--yao-meta-skill.md)
- **[sepia](https://github.com/Nanako0129/sepia)** - 改善 AI 寫作制式與冗長文風的 Agent Skill。 (⭐ 2,639)
  - [詳細說明](research-notes/Nanako0129--sepia.md)
- **[craft-skills](https://github.com/ZSeven-W/craft-skills)** - 以研究資料與評測結果設計的 Agent Skills 集合。 (⭐ 154)
  - [詳細說明](research-notes/ZSeven-W--craft-skills.md)
- **[SkillSpector](https://github.com/NVIDIA/SkillSpector)** - 在安裝前掃描 Agent Skills 潛在安全風險的工具。 (⭐ 17,398)
  - [詳細說明](research-notes/NVIDIA--SkillSpector.md)
- **[codex-keysmith](https://github.com/Jia-Ethan/codex-keysmith)** - 以版本化設定管理 Codex 指令與 hooks 的部署。 (⭐ 4,501)
  - [詳細說明](research-notes/Jia-Ethan--codex-keysmith.md)
- **[aidlc-workflows](https://github.com/awslabs/aidlc-workflows)** - 替多種 Coding Agent 提供結構化開發流程的範本。 (⭐ 4,652)
  - [詳細說明](research-notes/awslabs--aidlc-workflows.md)

- **[follow-builders](https://github.com/zarazhangrui/follow-builders)** - 定期彙整 AI 建構者貼文、播客與官方部落格的 Agent Skill。 (⭐ 6,807)
  - [詳細說明](research-notes/zarazhangrui--follow-builders.md)

### 其他 Agent 相關
- **[agentic-rag-for-dummies](https://github.com/GiovanniPasq/agentic-rag-for-dummies)** - 用 LangGraph 示範 Agentic RAG 組件與流程的教學專案。 (⭐ 4,172)
  - [詳細說明](research-notes/GiovanniPasq--agentic-rag-for-dummies.md)
- **[CL4R1T4S](https://github.com/elder-plinius/CL4R1T4S)** - 蒐集 AI 服務的系統提示、指引與工具定義的資料庫。 (⭐ 49,920)
  - [詳細說明](research-notes/elder-plinius--CL4R1T4S.md)
- **[openhuman](https://github.com/tinyhumansai/openhuman)** - 整合持續記憶、工具與排程的人機協作 Agent 平台。 (⭐ 39,817)
  - [詳細說明](research-notes/tinyhumansai--openhuman.md)
- **[HermesOffice](https://github.com/criptogus/HermesOffice)** - 支援文件、試算表與簡報的開源 AI 辦公軟體。 (⭐ 578)
  - [詳細說明](research-notes/criptogus--HermesOffice.md)
- **[openchamber](https://github.com/openchamber/openchamber)** - 以 OpenCode 為核心的 Agent 開發工作環境。 (⭐ 9,921)
  - [詳細說明](research-notes/openchamber--openchamber.md)
- **[Claude-Code-Game-Studios](https://github.com/Donchitos/Claude-Code-Game-Studios)** - 將 Claude Code 組成含企劃、程式、美術、QA 與發行流程的遊戲開發範本。 (⭐ 25,411)
  - [詳細說明](research-notes/Donchitos--Claude-Code-Game-Studios.md)
- **[gepa](https://github.com/gepa-ai/gepa)** - 利用 LLM 反思與評估結果，最佳化提示等文字參數。 (⭐ 6,599)
  - [詳細說明](research-notes/gepa-ai--gepa.md)
- **[llmfit](https://github.com/AlexsJones/llmfit)** - 依 CPU、GPU 與記憶體推薦可在本機執行的 LLM。 (⭐ 36,659)
  - [詳細說明](research-notes/AlexsJones--llmfit.md)
- **[headroom](https://github.com/headroomlabs-ai/headroom)** - 壓縮 Agent 上下文並協助共享記憶的工具。 (⭐ 72,423)
  - [詳細說明](research-notes/headroomlabs-ai--headroom.md)
- **[ruflo](https://github.com/ruvnet/ruflo)** - 供 Claude Code 與 Codex 使用的多 Agent 工作流程框架。 (⭐ 72,600)
  - [詳細說明](research-notes/ruvnet--ruflo.md)
- **[superpowers](https://github.com/obra/superpowers)** - 以可組合 Skills 規範 Agent 開發步驟的方法與工具。 (⭐ 287,485)
  - [詳細說明](research-notes/obra--superpowers.md)
- **[ponytail](https://github.com/DietrichGebert/ponytail)** - 用指引與 hooks 協助 Agent 控制工作複雜度。 (⭐ 140,002)
  - [詳細說明](research-notes/DietrichGebert--ponytail.md)

---

## 📚 學習資源與教程

### AI 基礎
- **[30u30](https://github.com/Ojhaharsh/30u30)** - 以 30 天的閱讀筆記、Notebook、從零實作與練習，引導學習 30 篇重要 AI 論文。 (⭐ 1,066)
  - [詳細說明](research-notes/Ojhaharsh--30u30.md)
- **[generative-ai-for-beginners](https://github.com/microsoft/generative-ai-for-beginners)** - 微軟的 21 課生成式 AI 入門課程，兼顧概念與實作。 (⭐ 119,863)
  - [詳細說明](research-notes/microsoft--generative-ai-for-beginners.md)
- **[Foundations-of-LLMs](https://github.com/ZJU-LLMs/Foundations-of-LLMs)** - 浙江大學團隊編寫、涵蓋模型原理與 RAG 的中文教材。 (⭐ 17,893)
  - [詳細說明](research-notes/ZJU-LLMs--Foundations-of-LLMs.md)
- **[LLMs-from-scratch](https://github.com/rasbt/LLMs-from-scratch)** - 搭配 PyTorch 實作的 LLM 原理教材，從模型架構學到微調。 (⭐ 105,076)
  - [詳細說明](research-notes/rasbt--LLMs-from-scratch.md)
- **[dive-into-llms](https://github.com/Lordog/dive-into-llms)** - 涵蓋大模型微調、部署與提示學習的中文實作教程。 (⭐ 54,403)
  - [詳細說明](research-notes/Lordog--dive-into-llms.md)
- **[AI-For-Beginners](https://github.com/microsoft/AI-For-Beginners)** - 微軟的 12 週 AI 入門課程，含閱讀、測驗與實驗。 (⭐ 68,574)
  - [詳細說明](research-notes/microsoft--AI-For-Beginners.md)

### Agent 專業
- **[AI Agent Handbook](https://github.com/aliyun/ai-agent-handbook)** - 阿里雲的開源 Agent 白皮書，整理架構、建構、運行、治理、評估及企業案例。 (⭐ 2,076)
  - [詳細說明](research-notes/aliyun--ai-agent-handbook.md)
- **[ai-agent-book](https://github.com/bojieli/ai-agent-book)** - 從 Agent 設計原理到工程實作的中文開源書與實驗。 (⭐ 47,959)
  - [詳細說明](research-notes/bojieli--ai-agent-book.md)
- **[awesome-agentic-ai-zh](https://github.com/WenyuChiou/awesome-agentic-ai-zh)** - 繁體中文 Agent 學習路線圖，含工具使用與建構者路線。 (⭐ 7,034)
  - [詳細說明](research-notes/WenyuChiou--awesome-agentic-ai-zh.md)
- **[agentic-design-patterns](https://github.com/xindoo/agentic-design-patterns)** - 介紹 21 種 Agent 設計模式的中文翻譯讀物。 (⭐ 8,020)
  - [詳細說明](research-notes/xindoo--agentic-design-patterns.md)
- **[Agentic-Design-Patterns](https://github.com/evoiz/Agentic-Design-Patterns)** - 以書籍 PDF 與 Notebook 練習 AI Agent 設計模式。 (⭐ 3,604)
  - [詳細說明](research-notes/evoiz--Agentic-Design-Patterns.md)
- **[learn-claude-code](https://github.com/shareAI-lab/learn-claude-code)** - 逐課拆解 Coding Agent 的工具、權限、記憶與工作流程。 (⭐ 76,948)
  - [詳細說明](research-notes/shareAI-lab--learn-claude-code.md)
- **[ai-engineering-from-scratch](https://github.com/rohitg00/ai-engineering-from-scratch)** - 從機器學習到 LLM、Agent 與部署的分階段自學課程。 (⭐ 54,774)
  - [詳細說明](research-notes/rohitg00--ai-engineering-from-scratch.md)

- **[AI Agents: The Definitive Guide](https://github.com/Nicolepcx/ai-agents-the-definitive-guide)** - 搭配書籍學習 Agent 架構、部署、評估、記憶與安全的 Notebook。 (⭐ 2,521)
  - [詳細說明](research-notes/Nicolepcx--ai-agents-the-definitive-guide.md)
- **[AI Engineering Interview Questions](https://github.com/pallavi-shekhar/ai-engineering-interview-questions-company-wise)** - 按公司與主題整理公開 AI 工程面試題目及準備方向。 (⭐ 1,502)
  - [詳細說明](research-notes/pallavi-shekhar--ai-engineering-interview-questions-company-wise.md)

- **[AI Agents for Beginners](https://github.com/microsoft/ai-agents-for-beginners)** - 以 18 課文字、影片與 Python 範例介紹 Agent 設計、工具、RAG、記憶、部署及安全。 (⭐ 76,049)
  - [詳細說明](research-notes/microsoft--ai-agents-for-beginners.md)

### 自我提升
- **[DeepTutor](https://github.com/HKUDS/DeepTutor)** - 可匯入個人資料、安排學習路徑、練習與對話的開源 AI 家教平台。 (⭐ 46,359)
  - [詳細說明](research-notes/HKUDS--DeepTutor.md)
- **[詞光 Word Atlas](https://github.com/designfuchen/word-atlas)** - 以插畫、發音、語境與間隔複習學習雅思詞彙的本機優先網站。 (⭐ 2,715)
  - [詳細說明](research-notes/designfuchen--word-atlas.md)
- **[WordLink](https://github.com/orionsheep/wordlink)** - 用詞彙關係圖、測驗與分級閱讀來記單字的開源英語學習工具。 (⭐ 245)
  - [詳細說明](research-notes/orionsheep--wordlink.md)
- **[book-en](https://github.com/craig7351/book-en)** - 可在桌面上用 YouTube 雙語字幕、逐句重播、查詞與間隔複習學英文的工具。 (⭐ 6)
  - [詳細說明](research-notes/craig7351--book-en.md)
- **[高性價比人生指南](https://github.com/eternity4719/HowToLiveBetter)** - 按健康、時間、金錢、法律與生活主題整理行動建議，標示成本、證據等級及來源。 (⭐ 69,082)
  - [詳細說明](research-notes/eternity4719--HowToLiveBetter.md)
- **[the-craft-of-selfteaching](https://github.com/selfteaching/the-craft-of-selfteaching)** - 用 Python 與寫作練習建立自學能力的開放教材。 (⭐ 16,819)
  - [詳細說明](research-notes/selfteaching--the-craft-of-selfteaching.md)
- **[xiaolai/the-craft-of-selfteaching](https://github.com/xiaolai/the-craft-of-selfteaching)** - 李笑來《自學是門手藝》的早期 Notebook 倉庫，結合自學方法與 Python 練習。 (⭐ 17,210)
  - [詳細說明](research-notes/xiaolai--the-craft-of-selfteaching.md)
- **[A-Programmers-Guide-to-English](https://github.com/yujiangshui/A-Programmers-Guide-to-English)** - 面向程式設計者的中文英語學習方法與資源指南。 (⭐ 16,691)
  - [詳細說明](research-notes/yujiangshui--A-Programmers-Guide-to-English.md)
- **[IELTS Atlas](https://github.com/gtiipoi/ielts-practice)** - 可在本機練習雅思閱讀與聽力，記錄成績、錯題與學習進度的純前端系統。 (⭐ 316)
  - [詳細說明](research-notes/gtiipoi--ielts-practice.md)
- **[awesome-english-ebooks](https://github.com/hehonghui/awesome-english-ebooks)** - 彙整《經濟學人》、《紐約客》等英文雜誌檔案與閱讀器建議的更新型資料庫。 (⭐ 36,936)
  - [詳細說明](research-notes/hehonghui--awesome-english-ebooks.md)
- **[time-as-a-friend](https://github.com/xiaolai/time-as-a-friend)** - 探討時間、思考與長期成長的《把時間當作朋友》線上讀物。 (⭐ 2,820)
  - [詳細說明](research-notes/xiaolai--time-as-a-friend.md)
- **[resources-to-become-a-great-engineering-leader](https://github.com/gregorojstersek/resources-to-become-a-great-engineering-leader)** - 依管理、技術與溝通主題整理的工程領導資源索引。 (⭐ 7,643)
  - [詳細說明](research-notes/gregorojstersek--resources-to-become-a-great-engineering-leader.md)
- **[FDE-the-Guidance-Book-of-Forward-Deployed-Engineer](https://github.com/xdash/FDE-the-Guidance-Book-of-Forward-Deployed-Engineer)** - 介紹 FDE 角色、客戶問題與交付流程的中文職涯指南。 (⭐ 4,724)
  - [詳細說明](research-notes/xdash--FDE-the-Guidance-Book-of-Forward-Deployed-Engineer.md)

### 系統設計
- **[system-design-notes](https://github.com/liquidslr/system-design-notes)** - 整理《System Design Interview》題目與觀念的非官方筆記。 (⭐ 20,018)
  - [詳細說明](research-notes/liquidslr--system-design-notes.md)

### 其他教程
- **[agents-from-scratch](https://github.com/langchain-ai/agents-from-scratch)** - 以郵件助理範例學習 Agent、評估、人工確認與記憶。 (⭐ 2,225)
  - [詳細說明](research-notes/langchain-ai--agents-from-scratch.md)
- **[rlhf-book-zh-tw](https://github.com/ai-twinkle/rlhf-book-zh-tw)** - 《Reinforcement Learning from Human Feedback》繁體中文譯本。 (⭐ 179)
  - [詳細說明](research-notes/ai-twinkle--rlhf-book-zh-tw.md)
- **[machine-learning-visualized](https://github.com/gavinkhung/machine-learning-visualized)** - 以互動 Notebook 展示模型訓練過程的機器學習教材。 (⭐ 1,964)
  - [詳細說明](research-notes/gavinkhung--machine-learning-visualized.md)
- **[ai-job-search](https://github.com/MadsLorentzen/ai-job-search)** - 以 Claude Code 協助評估職缺、客製履歷與準備面試。 (⭐ 43,071)
  - [詳細說明](research-notes/MadsLorentzen--ai-job-search.md)

---

## 🎨 設計與可視化工具

### 圖表和圖形
- **[figures4papers](https://github.com/ChenLiu-1996/figures4papers)** - 收錄論文等級圖表的 Python 程式、範例與科學製圖 Agent Skill。 (⭐ 9,263)
  - [詳細說明](research-notes/ChenLiu-1996--figures4papers.md)
- **[江山時序](https://github.com/DeanChensj/jiangshan-map)** - 以互動地圖與時間軸探索中國歷代疆域、古今地名、人物行跡與詩文路線。 (⭐ 1,414)
  - [詳細說明](research-notes/DeanChensj--jiangshan-map.md)
- **[SeeCode](https://github.com/Aryanutkarsh/SeeCode)** - 讓 Agent 將流程與資料做成可探索的動態圖，並匯出 HTML、圖片或影片。 (⭐ 421)
  - [詳細說明](research-notes/Aryanutkarsh--SeeCode.md)
- **[drawio-skill](https://github.com/Agents365-ai/drawio-skill)** - 將文字或專案資料轉成可編輯的 draw.io 圖，並支援同步更新與架構驗證。 (⭐ 10,002)
  - [詳細說明](research-notes/Agents365-ai--drawio-skill.md)
- **[lieflat-charts](https://github.com/larashero3-dotcom/lieflat-charts)** - 用 Agent Skill 把資料轉成 HTML 圖表或視覺報告。 (⭐ 5,470)
  - [詳細說明](research-notes/larashero3-dotcom--lieflat-charts.md)
- **[fireworks-tech-graph](https://github.com/yizhiyanhua-ai/fireworks-tech-graph)** - 依文字描述產生 SVG、PNG 架構圖與技術流程圖。 (⭐ 11,432)
  - [詳細說明](research-notes/yizhiyanhua-ai--fireworks-tech-graph.md)
- **[ppt-master](https://github.com/hugohe3/ppt-master)** - 讓 AI Agent 從文件製作可在 PowerPoint 編輯的簡報。 (⭐ 54,772)
  - [詳細說明](research-notes/hugohe3--ppt-master.md)
- **[awesome-gpt-image-2](https://github.com/freestylefly/awesome-gpt-image-2)** - 提供影像提示詞、案例與模板的資源庫。 (⭐ 32,221)
  - [詳細說明](research-notes/freestylefly--awesome-gpt-image-2.md)

- **[AetherViz Master](https://github.com/andyhuo520/aetherviz-master)** - 引導 Agent 將教學主題製成含 3D、圖表與互動控制的網頁。 (⭐ 1,495)
  - [詳細說明](research-notes/andyhuo520--aetherviz-master.md)

### 視覺內容
- **[claude-pxl](https://github.com/augusto-scarvalho/claude-pxl)** - 用程式描述像素藝術，並輸出 PNG、動畫與素材表的創作工具。 (⭐ 207)
  - [詳細說明](research-notes/augusto-scarvalho--claude-pxl.md)
- **[mesh-avatar-studio](https://github.com/shinshin86/mesh-avatar-studio)** - 把單張插圖變成可用臉部或聲音驅動的 2D 網格角色。 (⭐ 1,287)
  - [詳細說明](research-notes/shinshin86--mesh-avatar-studio.md)
- **[Motion Prompt](https://github.com/showheyohtaki/motion-prompt)** - 用動態範例庫查找動畫、鏡頭與 UI 效果名稱，協助向 AI 精確描述畫面。 (⭐ 67)
  - [詳細說明](research-notes/showheyohtaki--motion-prompt.md)
- **[Anatomy](https://github.com/wheresryan22/anatomy)** - 用 Agent 製作解釋機械與技術概念的互動等角插圖，可輸出 HTML 或 SVG。 (⭐ 8,763)
  - [詳細說明](research-notes/wheresryan22--anatomy.md)
- **[hand-drawn-styles](https://github.com/threerocks/hand-drawn-styles)** - 提供可重用的手繪畫風配方，讓 Agent 依內容產生生圖提示詞。 (⭐ 2,104)
  - [詳細說明](research-notes/threerocks--hand-drawn-styles.md)
- **[handraw-style](https://github.com/yang0/handraw-style)** - 用編號畫廊挑選手繪風格並產生對應提示詞。 (⭐ 1,972)
  - [詳細說明](research-notes/yang0--handraw-style.md)
- **[ian-xiaohei-illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations)** - 把中文文章內容轉成「小黑」風格正文插圖的 Skill。 (⭐ 11,722)
  - [詳細說明](research-notes/helloianneo--ian-xiaohei-illustrations.md)
- **[ip-as-logo-skill](https://github.com/s1dashu/ip-as-logo-skill)** - 協助 Agent 設計簡潔吉祥物 Logo 的 Skill。 (⭐ 5,288)
  - [詳細說明](research-notes/s1dashu--ip-as-logo-skill.md)
- **[srt-whiteboard-animation](https://github.com/geeklee/srt-whiteboard-animation)** - 依 SRT 字幕製作分鏡與白板手繪動畫的 Skill。 (⭐ 3,334)
  - [詳細說明](research-notes/geeklee--srt-whiteboard-animation.md)
- **[chinese-traditional-patterns](https://github.com/dososo/chinese-traditional-patterns)** - 提供傳統紋樣圖錄、寓意與應用資料的素材庫。 (⭐ 299)
  - [詳細說明](research-notes/dososo--chinese-traditional-patterns.md)

- **[LightCraft](https://github.com/storytold/lightcraft)** - 以 Rust 製作的本機照片管理與非破壞式 RAW 修圖工具，並支援 Agent 操作。 (⭐ 1,834)
  - [詳細說明](research-notes/storytold--lightcraft.md)

### 文檔和演示
- **[holo-card-studio](https://github.com/EverettFish/holo-card-studio)** - 用 Codex Skill 製作全息卡牌、Blender 工程與互動頁面。 (⭐ 1,558)
  - [詳細說明](research-notes/EverettFish--holo-card-studio.md)
- **[dashi-ppt-skill](https://github.com/chuspeeism/dashi-ppt-skill)** - 讓 Agent 產生可在瀏覽器編輯、可輸出 PPTX 的簡報。 (⭐ 8,302)
  - [詳細說明](research-notes/chuspeeism--dashi-ppt-skill.md)

---

## 🔍 RAG & 知識管理

### RAG 引擎
- **[DeepSearcher](https://github.com/zilliztech/deep-searcher)** - 把私有文件載入向量資料庫，結合檢索與 LLM 查詢、產生研究式回答的 Python 工具。 (⭐ 8,345)
  - [詳細說明](research-notes/zilliztech--deep-searcher.md)
- **[ragflow](https://github.com/infiniflow/ragflow)** - 可自架的 RAG 問答平台，整合文件解析、檢索與引用。 (⭐ 90,810)
  - [詳細說明](research-notes/infiniflow--ragflow.md)
- **[LEANN](https://github.com/StarTrail-org/LEANN)** - 節省索引儲存空間的本機向量檢索與個人 RAG 工具。 (⭐ 12,941)
  - [詳細說明](research-notes/StarTrail-org--LEANN.md)
- **[supermemory](https://github.com/supermemoryai/supermemory)** - 為 AI 助理與應用提供跨對話記憶、使用者檔案、RAG 搜尋和資料連接器。 (⭐ 30,805)
  - [詳細說明](research-notes/supermemoryai--supermemory.md)

### 知識庫管理
- **[史記知識庫](https://github.com/baojie/shiji-kb)** - 將《史記》人物、事件與地點標註並連成可跳轉、可搜尋的互動閱讀與知識圖譜。 (⭐ 3,469)
  - [詳細說明](research-notes/baojie--shiji-kb.md)
- **[llm_wiki](https://github.com/nashsu/llm_wiki)** - 匯入文件並持續建立連結與知識圖譜的桌面知識庫。 (⭐ 19,632)
  - [詳細說明](research-notes/nashsu--llm_wiki.md)
- **[obsidian-llm-wiki](https://github.com/GD4AI/obsidian-llm-wiki)** - 在 Obsidian 中用 AI 建立來源、概念頁與筆記連結的外掛。 (⭐ 626)
  - [詳細說明](research-notes/GD4AI--obsidian-llm-wiki.md)
- **[Understand-Anything](https://github.com/Egonex-AI/Understand-Anything)** - 把程式庫轉成互動知識圖，輔助理解依賴與變更影響。 (⭐ 83,035)
  - [詳細說明](research-notes/Egonex-AI--Understand-Anything.md)
- **[knowledge-catalog](https://github.com/GoogleCloudPlatform/knowledge-catalog)** - 展示 Google Cloud 資料目錄工具、Agent 與範例的倉庫。 (⭐ 9,214)
  - [詳細說明](research-notes/GoogleCloudPlatform--knowledge-catalog.md)

- **[Hyper-Extract](https://github.com/yifanfeng97/Hyper-Extract)** - 將文件擷取成可追溯的圖譜、超圖等知識結構，並可匯出 Obsidian。 (⭐ 4,026)
  - [詳細說明](research-notes/yifanfeng97--Hyper-Extract.md)
- **[OpenKB](https://github.com/VectifyAI/OpenKB)** - 將 PDF、Office、網頁等資料持續編譯成互相連結的 Markdown Wiki，並支援 Query、Chat、知識圖與 Agent Skill 生成。
  - [詳細說明](research-notes/VectifyAI--OpenKB.md)

### 文檔處理
- **[MinerU](https://github.com/opendatalab/MinerU)** - 解析 PDF、掃描圖與 Office 文件，供 Agent 定位和讀取內容。 (⭐ 80,038)
  - [詳細說明](research-notes/opendatalab--MinerU.md)
- **[Unlimited-OCR](https://github.com/baidu/Unlimited-OCR)** - 供開發者整合圖片與 PDF 文字辨識的 OCR 模型專案。 (⭐ 25,717)
  - [詳細說明](research-notes/baidu--Unlimited-OCR.md)
- **[Umi-OCR](https://github.com/hiroi-sora/Umi-OCR)** - 支援截圖、批次文件辨識與 QR Code 的免費離線 OCR 軟體。 (⭐ 47,340)
  - [詳細說明](research-notes/hiroi-sora--Umi-OCR.md)
- **[PDFMathTranslate](https://github.com/PDFMathTranslate/PDFMathTranslate)** - 翻譯學術 PDF 並盡量保留公式、圖表與原版面。 (⭐ 36,997)
  - [詳細說明](research-notes/PDFMathTranslate--PDFMathTranslate.md)
- **[liteparse](https://github.com/run-llama/liteparse)** - 把 PDF 等文件解析成 Markdown、文字或結構化資料。 (⭐ 12,316)
  - [詳細說明](research-notes/run-llama--liteparse.md)
- **[pdf-inspector](https://github.com/firecrawl/pdf-inspector)** - 快速判斷 PDF 是文字型、掃描型或混合型，並將可解析內容轉成結構化 Markdown。 (⭐ 19,238)
  - [詳細說明](research-notes/firecrawl--pdf-inspector.md)
- **[opendataloader-pdf](https://github.com/opendataloader-project/opendataloader-pdf)** - 輸出 Markdown 或 JSON 的跨語言 PDF 解析工具。 (⭐ 29,286)
  - [詳細說明](research-notes/opendataloader-project--opendataloader-pdf.md)
- **[KillerPDF](https://github.com/SteveTheKiller/KillerPDF)** - 可用圖形介面編輯 PDF 的免費開源軟體。 (⭐ 3,864)
  - [詳細說明](research-notes/SteveTheKiller--KillerPDF.md)
- **[ky-markdown-rebuilder](https://github.com/KyrieCheungYep/ky-markdown-rebuilder)** - 逐頁檢查並重建複雜 PDF、投影片與掃描件的 Markdown。 (⭐ 118)
  - [詳細說明](research-notes/KyrieCheungYep--ky-markdown-rebuilder.md)
- **[markitdown](https://github.com/microsoft/markitdown)** - 將 PDF、Office、HTML 等內容轉成供 LLM 使用的 Markdown。 (⭐ 184,691)
  - [詳細說明](research-notes/microsoft--markitdown.md)

### 其他 RAG 相關
- **[AutoRAG](https://github.com/Marker-Inc-Korea/AutoRAG)** - 新版為整理文件知識的館員 Agent；舊版 RAG 最佳化工具另存。 (⭐ 5,073)
  - [詳細說明](research-notes/Marker-Inc-Korea--AutoRAG.md)
- **[qiaomu-anything-to-notebooklm](https://github.com/joeseesun/qiaomu-anything-to-notebooklm)** - 整理文章、影音與文件後送入 NotebookLM 的 Agent Skill。 (⭐ 5,994)
  - [詳細說明](research-notes/joeseesun--qiaomu-anything-to-notebooklm.md)
- **[turbovec](https://github.com/RyanCodrai/turbovec)** - 以 TurboQuant 壓縮向量的 Rust 索引元件，供檢索管線使用。 (⭐ 17,193)
  - [詳細說明](research-notes/RyanCodrai--turbovec.md)

---

## 💻 開發工具與效率

### 代碼審查與質量
- **[open-code-review](https://github.com/alibaba/open-code-review)** - 結合規則選檔與 LLM 判斷的本機程式碼審查工具。 (⭐ 30,647)
  - [詳細說明](research-notes/alibaba--open-code-review.md)
- **[spec-kit](https://github.com/github/spec-kit)** - 為 Coding Agent 提供規格範本與決策紀錄的開發工具組。 (⭐ 137,255)
  - [詳細說明](research-notes/github--spec-kit.md)
- **[ECC](https://github.com/affaan-m/ECC)** - 整合 Agent 規則、Skills、hooks 與工作流程的開發環境集合。 (⭐ 259,793)
  - [詳細說明](research-notes/affaan-m--ECC.md)

### 代碼理解
- **[Graphify](https://github.com/Graphify-Labs/graphify)** - 在本機解析程式碼及文件，建立可查詢的關係圖，供 Coding Agent 追查呼叫路徑與系統脈絡。 (⭐ 135,384)
  - [詳細說明](research-notes/Graphify-Labs--graphify.md)
- **[REA](https://github.com/morluto/rea)** - 透過 MCP 與命令列分析應用、網站及執行檔，追查功能並附上證據。 (⭐ 27,048)
  - [詳細說明](research-notes/morluto--rea.md)
- **[codeflow](https://github.com/braedonsaunders/codeflow)** - 貼上 GitHub 網址即可查看程式依賴與影響範圍的架構圖。 (⭐ 5,207)
  - [詳細說明](research-notes/braedonsaunders--codeflow.md)
- **[birdview](https://github.com/Qiuner/birdview)** - 讓 Coding Agent 在改程式前建立架構地圖並標出預計影響範圍的 Skill。 (⭐ 367)
  - [詳細說明](research-notes/Qiuner--birdview.md)

- **[Ix](https://github.com/ix-infrastructure/Ix)** - 將程式庫建成持久系統圖，供人與 Coding Agent 查詢流程及修改影響。 (⭐ 999)
  - [詳細說明](research-notes/ix-infrastructure--Ix.md)
- **[Graft](https://github.com/trailhq/Graft)** - 建立本機程式碼上下文圖，為多種 Coding Agent 提供相關結構資訊。 (⭐ 9,320)
  - [詳細說明](research-notes/trailhq--Graft.md)

### 內容提取與爬蟲
- **[crawl4ai](https://github.com/unclecode/crawl4ai)** - 將網頁擷取、清理成適合 LLM 使用的 Markdown。 (⭐ 83,663)
  - [詳細說明](research-notes/unclecode--crawl4ai.md)
- **[Scrapling](https://github.com/D4Vinci/Scrapling)** - 支援動態頁面與爬行流程的 Python 網頁擷取框架。 (⭐ 81,343)
  - [詳細說明](research-notes/D4Vinci--Scrapling.md)
- **[instaloader](https://github.com/instaloader/instaloader)** - 下載 Instagram 可存取的媒體與中繼資料的命令列工具。 (⭐ 13,387)
  - [詳細說明](research-notes/instaloader--instaloader.md)
- **[TwitterMediaHarvest](https://github.com/EltonChou/TwitterMediaHarvest)** - 下載 X／Twitter 圖片與影片的瀏覽器擴充功能。 (⭐ 1,169)
  - [詳細說明](research-notes/EltonChou--TwitterMediaHarvest.md)
- **[CloakBrowser](https://github.com/CloakHQ/CloakBrowser)** - 調整瀏覽器指紋、供自動化使用的 Chromium 工具。 (⭐ 31,497)
  - [詳細說明](research-notes/CloakHQ--CloakBrowser.md)

- **[patchright-enhanced](https://github.com/whaleyxbt/patchright-enhanced)** - 以 Patchright 啟動帶代理與基本隱匿設定的 Chrome 自動化工作階段。 (⭐ 339)
  - [詳細說明](research-notes/whaleyxbt--patchright-enhanced.md)

### 會議與記錄
- **[recensa](https://github.com/S40911120/recensa)** - 搜尋與重播 Claude Code 工作紀錄的自架網頁檢視器。 (⭐ 72)
  - [詳細說明](research-notes/S40911120--recensa.md)
- **[ownscribe](https://github.com/nczz/ownscribe)** - 偏重繁中與中英混合會議的本機轉錄與摘要 CLI。 (⭐ 178)
  - [詳細說明](research-notes/nczz--ownscribe.md)

### 編輯與排版
- **[markdown-online-editor](https://github.com/nicejade/markdown-online-editor)** - 提供即時預覽與圖表支援的線上 Markdown 編輯器。 (⭐ 3,971)
  - [詳細說明](research-notes/nicejade--markdown-online-editor.md)
- **[commentflow](https://github.com/sysprog21/commentflow)** - 重排 C、C++、Rust 與 Shell 程式註解的換行格式。 (⭐ 27)
  - [詳細說明](research-notes/sysprog21--commentflow.md)

---

## 🎬 視頻/音頻/內容生成
- **[小說工作台 Novel Studio](https://github.com/yamasoo/novel-studio)** - 用本機介面與可選 AI 維護繁體中文長篇小說的設定、章綱、候選稿、伏筆及匯出流程。 (⭐ 4)
  - [詳細說明](research-notes/yamasoo--novel-studio.md)
- **[Translation Gateway](https://github.com/rictirse/TranslationGateway)** - 配合 PotPlayer 與自選 LLM，將日文影片或直播字幕即時轉成繁體中文，並管理術語及修正紀錄。 (⭐ 23)
  - [詳細說明](research-notes/rictirse--TranslationGateway.md)

### 開源影片剪輯與 AI 剪片
- **[ReelMimic](https://github.com/edenfunf/reelmimic)** - 分析參考影片的節奏與畫風，再用 Codex 或 Claude Code 製作新的 2D 動畫。 (⭐ 239)
  - [詳細說明](research-notes/edenfunf--reelmimic.md)
- **[VoiceStudio](https://github.com/debpalash/VoiceStudio)** - 可在本機配音、轉錄、聲音設計與影片配音的跨平台語音工作室。 (⭐ 91,692)
  - [詳細說明](research-notes/debpalash--VoiceStudio.md)
- **[ClaudeAnimationBase](https://github.com/JohnHeibel/ClaudeAnimationBase)** - 用 p5.js、p5.brush 與角色素材，讓 Coding Agent 製作手繪卡通影片的起始套件。 (⭐ 2,172)
  - [詳細說明](research-notes/JohnHeibel--ClaudeAnimationBase.md)
- **[mg-styles-15](https://github.com/Vincentwei1021/mg-styles-15)** - 展示 15 種程式製作的 10 秒動態設計影片，附提示詞與完整來源。 (⭐ 2,460)
  - [詳細說明](research-notes/Vincentwei1021--mg-styles-15.md)
- **[video-shotcraft](https://github.com/Vincentwei1021/video-shotcraft)** - 用 Codex 或 Claude Code 的 Skill，將真實產品截圖製成可編輯的宣傳短片。 (⭐ 14,162)
  - [詳細說明](research-notes/Vincentwei1021--video-shotcraft.md)
- **[HyperFrames](https://github.com/heygen-com/hyperframes)** - 讓 Coding Agent 以 HTML 與網頁元件製作、預覽及渲染影片的框架。 (⭐ 74,077)
  - [詳細說明](research-notes/heygen-com--hyperframes.md)
- **[lemo-opuscar](https://github.com/lemomo-ai/lemo-opuscar)** - 提供 59 種可套用與自訂的程式製片風格，供 Claude Code 製作影片。 (⭐ 8,769)
  - [詳細說明](research-notes/lemomo-ai--lemo-opuscar.md)
- **[animate](https://github.com/cth9191/animate)** - 讓 Claude Code 依分鏡與風格提示，製作可輸出 MP4 的程式動畫 Skill。 (⭐ 1,019)
  - [詳細說明](research-notes/cth9191--animate.md)
- **[AutoClip](https://github.com/zhouxiaoka/autoclip)** - AI 自動分析長影片、找出值得剪的片段，產生短影音、字幕、封面與發布文案；適合 Podcast、訪談與 YouTube 長片再利用。 (⭐ 9,765)
  - [詳細說明](research-notes/zhouxiaoka--autoclip.md)
- **[Concat](https://github.com/jub0t/Concat)** - Local-first 的開源 CapCut 替代品，提供多軌時間軸、自動字幕、配音、去背、4K 輸出，並支援 MCP 與 JSON-RPC；目前 Beta 但已能實際使用。 (⭐ 11,852)
  - [詳細說明](research-notes/jub0t--Concat.md)
- **[OpenCut](https://github.com/OpenCut-app/OpenCut)** - 開源 CapCut 替代方案；新版正在從頭重寫，規劃 Plugin-first、Editor API、MCP、Headless 與 Scripting，現階段較適合收藏追蹤。 (⭐ 96,419)
  - [詳細說明](research-notes/OpenCut-app--OpenCut.md)
- **[AutoClip vs Concat vs OpenCut：三者比較與選擇指南](research-notes/comparison--AutoClip-vs-Concat-vs-OpenCut.md)** - AutoClip 偏 AI 自動選精華；Concat 偏現在可用的本機完整剪輯器；OpenCut 偏未來可擴充、可程式化的剪輯平台。

- **[MoneyPrinterTurbo](https://github.com/harry0703/MoneyPrinterTurbo)** - 從主題生成腳本、素材、配音與字幕，合成短影片的自架工具。 (⭐ 131,878)
  - [詳細說明](research-notes/harry0703--MoneyPrinterTurbo.md)
- **[chinese-novelist-skill](https://github.com/PenglongHuang/chinese-novelist-skill)** - 引導 Agent 規劃人物與章節，逐章撰寫並檢查中文長篇小說。 (⭐ 3,865)
  - [詳細說明](research-notes/PenglongHuang--chinese-novelist-skill.md)
- **[huashu-art-motion](https://github.com/alchaincyf/huashu-art-motion)** - 讓 Agent 用程式製作藝術動畫與解說片段，提供畫風和動畫語法範例。 (⭐ 2,467)
  - [詳細說明](research-notes/alchaincyf--huashu-art-motion.md)
- **[yt-dlp](https://github.com/yt-dlp/yt-dlp)** - 支援多個網站的命令列影音下載工具，可選格式、字幕與輸出方式。 (⭐ 196,229)
  - [詳細說明](research-notes/yt-dlp--yt-dlp.md)
- **[MeTube](https://github.com/alexta69/metube)** - 在瀏覽器貼網址並以自架服務下載影音的 yt-dlp 網頁介面。 (⭐ 14,948)
  - [詳細說明](research-notes/alexta69--metube.md)

- **[lanshu-create-ai-presenter-video](https://github.com/cclank/lanshu-create-ai-presenter-video)** - 用 Agent Skill 製作數位主持人或風格化解說影片，包含試片與成片驗證。 (⭐ 2,522)
  - [詳細說明](research-notes/cclank--lanshu-create-ai-presenter-video.md)
- **[OpenMontage](https://github.com/calesthio/OpenMontage)** - 用 AI Agent 規劃鏡頭、素材與剪輯的開源影片製作流程。 (⭐ 59,477)
  - [詳細說明](research-notes/calesthio--OpenMontage.md)
- **[Echo-Loop](https://github.com/echo-loop/Echo-Loop)** - 以精聽、跟讀、復述與複習練習英語聽說的 App。 (⭐ 3,546)
  - [詳細說明](research-notes/echo-loop--Echo-Loop.md)
- **[VidBee](https://github.com/nexmoe/VidBee)** - 提供影音下載、RSS 追蹤與本機語音轉錄的應用程式。 (⭐ 10,647)
  - [詳細說明](research-notes/nexmoe--VidBee.md)
- **[wenyi](https://github.com/BigDawnGhost/wenyi)** - 維護術語與全書脈絡的長篇書籍 AI 翻譯工具。 (⭐ 2,602)
  - [詳細說明](research-notes/BigDawnGhost--wenyi.md)
- **[DashPlayer](https://github.com/solidSpoon/DashPlayer)** - 結合雙語字幕、逐句精聽、查詞與本機字幕生成的英語學習播放器。 (⭐ 4,465)
  - [詳細說明](research-notes/solidSpoon--DashPlayer.md)

- **[story-to-handdrawn-video](https://github.com/gnipbao/story-to-handdrawn-video)** - 讓 Agent 將中文故事或圖片製成手繪日記漫畫風格的直式靜音動畫。 (⭐ 2,131)
  - [詳細說明](research-notes/gnipbao--story-to-handdrawn-video.md)


---

## 💰 金融與投資
- **[Awesome-Quant-Machine-Learning-Trading](https://github.com/grananqvist/Awesome-Quant-Machine-Learning-Trading)** - 彙整量化交易與金融機器學習的書籍、課程、論文及程式資源。 (⭐ 4,062)
  - [詳細說明](research-notes/grananqvist--Awesome-Quant-Machine-Learning-Trading.md)

- **[qlib](https://github.com/microsoft/qlib)** - 涵蓋資料準備、模型訓練與回測的量化投資研究平台。 (⭐ 48,606)
  - [詳細說明](research-notes/microsoft--qlib.md)
- **[wealth-tracker](https://github.com/nicejade/wealth-tracker)** - 記錄、分析個人資產並提供 AI 解讀的應用程式。 (⭐ 905)
  - [詳細說明](research-notes/nicejade--wealth-tracker.md)
- **[Financial_freedom](https://github.com/codeman008/Financial_freedom)** - 彙整理財與投資書籍、工具和社群的資源清單。 (⭐ 3,823)
  - [詳細說明](research-notes/codeman008--Financial_freedom.md)
- **[FinceptTerminal](https://github.com/Fincept-Corporation/FinceptTerminal)** - 提供市場資料、投資研究與分析介面的桌面金融終端。 (⭐ 31,690)
  - [詳細說明](research-notes/Fincept-Corporation--FinceptTerminal.md)
- **[OpenStock](https://github.com/Open-Dev-Society/OpenStock)** - 可自架的股票追蹤與研究平台，提供行情、圖表、觀察清單、提醒及公司資訊。 (⭐ 18,179)
  - [詳細說明](research-notes/Open-Dev-Society--OpenStock.md)
- **[awesome-systematic-trading](https://github.com/wangzhe3224/awesome-systematic-trading)** - 彙整回測、資料、因子、風險與實盤工具的系統化交易資源清單。 (⭐ 5,213)
  - [詳細說明](research-notes/wangzhe3224--awesome-systematic-trading.md)


---

## 📖 資源合集

- **[awesome](https://github.com/sindresorhus/awesome)** - 各領域精選資源清單的總索引。 (⭐ 506,592)
  - [詳細說明](research-notes/sindresorhus--awesome.md)
- **[HelloGitHub](https://github.com/521xueweihan/HelloGitHub)** - 以中文定期介紹有趣、易上手開源專案的內容集合。 (⭐ 176,872)
  - [詳細說明](research-notes/521xueweihan--HelloGitHub.md)
- **[the-book-of-secret-knowledge](https://github.com/trimstray/the-book-of-secret-knowledge)** - 供系統管理、開發與資安查閱的工具與指令速查集。 (⭐ 244,092)
  - [詳細說明](research-notes/trimstray--the-book-of-secret-knowledge.md)
- **[awesome-llm-apps](https://github.com/Shubhamsaboo/awesome-llm-apps)** - 彙整 Agent、RAG 與其他 LLM 應用的範例專案。 (⭐ 138,459)
  - [詳細說明](research-notes/Shubhamsaboo--awesome-llm-apps.md)
- **[awesome-vibe-coding](https://github.com/filipecalegario/awesome-vibe-coding)** - 彙整 AI 協作寫程式工具與資源的分類清單。 (⭐ 5,257)
  - [詳細說明](research-notes/filipecalegario--awesome-vibe-coding.md)
- **[vibe-coding-cn](https://github.com/tradecatlabs/vibe-coding-cn)** - 介紹 AI 協作開發、驗證與審查流程的中文指南。 (⭐ 16,251)
  - [詳細說明](research-notes/tradecatlabs--vibe-coding-cn.md)
- **[awesome-opus5-5-videos](https://github.com/yihui-dev/awesome-opus5-5-videos)** - 蒐集 Claude Opus 5.5 生成影片案例、原始作品與可重用提示詞。 (⭐ 1,347)
  - [詳細說明](research-notes/yihui-dev--awesome-opus5-5-videos.md)


---

## 🔧 其他實用工具

### 系統與應用
- **[GameNative](https://github.com/utkarshdalal/GameNative)** - 在 Android 裝置本機執行已擁有的 PC 遊戲，並支援控制器與雲端存檔。 (⭐ 11,035)
  - [詳細說明](research-notes/utkarshdalal--GameNative.md)
- **[OpenFace](https://github.com/TadasBaltrusaitis/OpenFace)** - 從影片或 webcam 擷取臉部特徵點、頭部姿態、動作單元及視線的研究工具。 (⭐ 7,783)
  - [詳細說明](research-notes/TadasBaltrusaitis--OpenFace.md)
- **[syncthing](https://github.com/syncthing/syncthing)** - 讓多台裝置持續同步檔案的開源工具。 (⭐ 88,644)
  - [詳細說明](research-notes/syncthing--syncthing.md)
- **[harness](https://github.com/harness/harness)** - 整合程式碼託管與 DevOps 流水線的開源交付平台。 (⭐ 38,366)
  - [詳細說明](research-notes/harness--harness.md)
- **[harness-engineering](https://github.com/deusyu/harness-engineering)** - 整理長時間 Agent 工作環境設計的中文學習資料。 (⭐ 5,942)
  - [詳細說明](research-notes/deusyu--harness-engineering.md)
- **[self-harness](https://github.com/datawhalechina/self-harness)** - 用實作範例介紹 Agent 工具、記憶與驗證的中文指南。 (⭐ 254)
  - [詳細說明](research-notes/datawhalechina--self-harness.md)
- **[compound-engineering-plugin](https://github.com/EveryInc/compound-engineering-plugin)** - 把工程經驗回饋為可重用 Skills 的 Agent 工作流程外掛。 (⭐ 25,103)
  - [詳細說明](research-notes/EveryInc--compound-engineering-plugin.md)
- **[planning-with-files](https://github.com/OthmanAdi/planning-with-files)** - 讓 Coding Agent 用檔案記錄長任務計畫、發現與進度。 (⭐ 26,934)
  - [詳細說明](research-notes/OthmanAdi--planning-with-files.md)
- **[career-ops](https://github.com/career-ops-hq/career-ops)** - 在本機 AI CLI 中評估職缺、調整履歷與追蹤申請。 (⭐ 71,795)
  - [詳細說明](research-notes/career-ops-hq--career-ops.md)

- **[TREK](https://github.com/liketrek/TREK)** - 可自架、支援多人協作、地圖、預算與清單的旅行規劃 Web 應用。 (⭐ 14,411)
  - [詳細說明](research-notes/liketrek--TREK.md)

### 簡歷與個人品牌
- **[magic-resume](https://github.com/JOYCEQL/magic-resume)** - 提供即時預覽、主題與 PDF 匯出的開源履歷編輯器。 (⭐ 10,571)
  - [詳細說明](research-notes/JOYCEQL--magic-resume.md)

### 其他
- **[Video-shortcraft](https://github.com/carlosciarrinovideo1-svg/Video-shortcraft)** - 名稱像影片工具，但目前 README 與檔案實際介紹 PentestGPT 滲透測試工具；用途需再核實。 (⭐ 17)
  - [詳細說明](research-notes/carlosciarrinovideo1-svg--Video-shortcraft.md)
- **[紫微斗數排盤引擎](https://github.com/Renhuai123/ziwei-doushu)** - 開源紫微斗數排盤演算法、古籍資料與示範介面，可查看命盤及研究不同排盤口徑。 (⭐ 7,796)
  - [詳細說明](research-notes/Renhuai123--ziwei-doushu.md)
- **[airi](https://github.com/moeru-ai/airi)** - 結合文字、語音與角色視覺的開源 AI 陪伴互動專案。 (⭐ 49,181)
  - [詳細說明](research-notes/moeru-ai--airi.md)
- **[up](https://github.com/byoungd/up)** - 持續更新的人生、學習與 AI 時代實作主題中文書稿。 (⭐ 62,840)
  - [詳細說明](research-notes/byoungd--up.md)
- **[lecture-to-notes](https://github.com/drpwchen/lecture-to-notes)** - 把講座影音與投影片整理成有來源依據的筆記。 (⭐ 103)
  - [詳細說明](research-notes/drpwchen--lecture-to-notes.md)
- **[niamos](https://github.com/pricklywiggles/niamos)** - 包含範本、查詢、儀表板與 Skills 的 Obsidian 庫組織系統。 (⭐ 192)
  - [詳細說明](research-notes/pricklywiggles--niamos.md)
- **[whichllm](https://github.com/Andyyyy64/whichllm)** - 依本機硬體估算適合執行哪些 LLM 的命令列工具。 (⭐ 6,644)
  - [詳細說明](research-notes/Andyyyy64--whichllm.md)
- **[egos-2000](https://github.com/yhzhang0128/egos-2000)** - 搭配教材與練習的微型教學作業系統。 (⭐ 3,616)
  - [詳細說明](research-notes/yhzhang0128--egos-2000.md)
- **[Horizon](https://github.com/Thysrael/Horizon)** - 彙整多個來源並產生個人每日閱讀簡報的工具。 (⭐ 9,368)
  - [詳細說明](research-notes/Thysrael--Horizon.md)
- **[heretic](https://github.com/p-e-w/heretic)** - 研究與修改本機語言模型拒答行為的工具。 (⭐ 31,552)
  - [詳細說明](research-notes/p-e-w--heretic.md)
- **[BD2-L2D-Viewer](https://github.com/Jelosus2/BD2-L2D-Viewer)** - 檢視《Brown Dust 2》角色 Live2D／Spine 動畫的網頁工具。 (⭐ 494)
  - [詳細說明](research-notes/Jelosus2--BD2-L2D-Viewer.md)
- **[AIHOT](https://github.com/KKKKhazix/AIHOT)** - 可自架並自訂信源、篩選標準、事件聚簇與日報的行業熱點網站框架。 (⭐ 3,867)
  - [詳細說明](research-notes/KKKKhazix--AIHOT.md)


---

## 📊 統計數據

- **Total Stars**: 220 repositories
- **Highest Stars**: awesome (506,592 ⭐)
- **Main Categories**: AI/Agent (40%), Learning Resources (15%), Design & Visualization (15%), RAG & Knowledge (10%), Tools (20%)

---

## 📝 說明

此列表是根據個人 GitHub Stars 進行分類整理。分類基於每個項目的主要功能和應用領域。

如需更新或有建議，歡迎提 Issue 或 PR！

**最後更新**：2026-10-28
