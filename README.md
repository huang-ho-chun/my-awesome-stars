# 🌟 My Awesome Stars Collection

個人精選 GitHub Stars，按分類整理。涵蓋 AI Agent、LLM、數據可視化、知識管理、開發工具等多個領域。

**Last Updated**: 2026-09-16

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
- **[Langflow](https://github.com/langflow-ai/langflow)** - Powerful tool for building and deploying AI-powered agents and workflows. (⭐ 154,880)
- **[DSPy](https://github.com/stanfordnlp/dspy)** - The framework for programming—not prompting—language models. (⭐ 38,065)
- **[SkillOpt](https://github.com/microsoft/SkillOpt)** - Text-space optimizer that trains reusable natural-language skills for frozen LLM agents. (⭐ 17,154)
  - **研究摘要**：這是改善 AI Agent Skill 的文字優化工具，從任務成敗找出修改方向，再用驗證任務檢查是否真的變好。
  - **適合你／怎麼用**：適合用來改進你反覆使用的 Codex Skills 與工作規範；可先看從歷史工作紀錄學習的 SkillOpt-Sleep，再決定是否導入完整訓練流程。
  - [詳細說明](research-notes/microsoft--SkillOpt.md)
- **[OpenMAIC](https://github.com/THU-MAIC/OpenMAIC)** - Open Multi-Agent Interactive Classroom — Get an immersive, multi-agent learning experience. (⭐ 37,318)
- **[Hermes Agent](https://github.com/NousResearch/hermes-agent)** - The open-source Hermes Agent. (⭐ 246,062)
- **[Hermes Desktop](https://github.com/fathah/hermes-desktop)** - Desktop version of Hermes Agent. (⭐ 14,231)

### Agent 工具
- **[context-mode](https://github.com/mksglu/context-mode)** - Context window optimization for AI coding agents. (⭐ 23,185)
- **[i-have-adhd](https://github.com/ayghri/i-have-adhd)** - Skill to stop your coding agent from burying the answer. ADHD-friendly output. (⭐ 46,685)
  - **研究摘要**：這是調整 Coding Agent 回答方式的 Skill：先給下一步、清楚編號並保留目前進度，避免重點埋在長篇說明中。
  - **適合你／怎麼用**：適合你與 Codex 多輪除錯時使用；可依自己的偏好改寫規則，讓每輪都交代已確認事項與下一個動作。
  - [詳細說明](research-notes/ayghri--i-have-adhd.md)
- **[GitNexus](https://github.com/abhigyanpatwari/GitNexus)** - The Zero-Server Code Intelligence Engine. (⭐ 47,380)
- **[Agent-Reach](https://github.com/Panniantong/Agent-Reach)** - Give your AI agent eyes to see the entire internet. (⭐ 82,337)
- **[codegraph](https://github.com/colbymchenry/codegraph)** - Pre-indexed code knowledge graph for Claude Code, Codex, Gemini, Cursor, OpenCode, AntiGravity. (⭐ 71,127)
  - **研究摘要**：這是替程式庫建立符號、呼叫與相依關係索引的工具，讓 Coding Agent 能查詢程式碼關係及修改影響範圍。
  - **適合你／怎麼用**：適合你處理跨多個檔案的報告流程或測試工具時，先索引專案，再請 Agent 查函式呼叫路徑與相關模組。
  - [詳細說明](research-notes/colbymchenry--codegraph.md)
- **[context-hub](https://github.com/andrewyng/context-hub)** - Context management for AI agents. (⭐ 13,981)

### 多模態
- **[CosyVoice](https://github.com/QwenAudio/CosyVoice)** - Multi-lingual large voice generation model. (⭐ 23,641)
- **[Seedance 2.0](https://github.com/Emily2040/seedance-2.0)** - Comprehensive production pipeline for quad-modal AI filmmaking. (⭐ 7,342)
- **[claude-video](https://github.com/bradautomates/claude-video)** - Give Claude the ability to watch any video. (⭐ 17,268)
- **[book-to-skill](https://github.com/virgiliojr94/book-to-skill)** - Turn any technical book PDF into a Claude Code skill. (⭐ 30,879)
  - **研究摘要**：這是把技術書或文件整理成可重複使用的 Agent Skill 的工具，將核心指引與詳細章節分開供 Agent 按需讀取。
  - **適合你／怎麼用**：適合把常查的 Linux、效能或軟體架構資料變成 Codex 的參考 Skill；先確認產出的索引與內容，再用實際問題測試。
  - [詳細說明](research-notes/virgiliojr94--book-to-skill.md)
- **[VoxCPM](https://github.com/OpenBMB/VoxCPM)** - Voice-based language model. (⭐ 37,639)
- **[VibeVoice](https://github.com/microsoft/VibeVoice)** - Open-Source Frontier Voice AI. (⭐ 54,336)

### Agent Skills
- **[archify](https://github.com/tt-a1i/archify)** - Beautiful, verifiable architecture, workflow, sequence, data-flow diagrams. (⭐ 64,422)
- **[diagram-design](https://github.com/cathrynlavery/diagram-design)** - 38 editorial diagram types for Claude Code, Codex, and Pi. (⭐ 40,413)
- **[effective-html](https://github.com/plannotator/effective-html)** - Agent skills for useful HTML artifacts, wireframes, interactive prototypes. (⭐ 3,190)
  - **研究摘要**：這是一組教 Coding Agent 製作 HTML 資訊成品的 Skills，涵蓋圖解、線框圖、可操作原型與視覺化計畫。
  - **適合你／怎麼用**：適合把你的測試流程、報告架構或方案比較做成可開啟的頁面；需要看流程時可從 `html-diagram` 開始。
  - [詳細說明](research-notes/plannotator--effective-html.md)
- **[flint-chart](https://github.com/microsoft/flint-chart)** - Visualization language for AI agents to create expressive charts. (⭐ 4,215)
  - **研究摘要**：這是供 AI Agent 使用的圖表描述與生成層，讓 Agent 指定資料意義和圖表需求，再處理座標軸、標籤與版面等細節。
  - **適合你／怎麼用**：適合把測試數據接到自動報告流程，產生可閱讀的效能比較圖；先用一份 CSV 試作並核對圖表與原始數值。
  - [詳細說明](research-notes/microsoft--flint-chart.md)
- **[cangjie-skill](https://github.com/kangarooking/cangjie-skill)** - Distill high-value content into executable Agent Skills. (⭐ 10,145)
- **[dashi-ppt-skill](https://github.com/chuspeeism/dashi-ppt-skill)** - AI-agent skill for browser-editable presentations. (⭐ 8,302)
- **[holo-card-studio](https://github.com/EverettFish/holo-card-studio)** - Turn descriptions into Blender card and interactive Three.js page. (⭐ 1,558)
- **[skills](https://github.com/emilkowalski/skills)** - Skills for Designers and Engineers. (⭐ 38,203)
  - **研究摘要**：這是一組給 Coding Agent 的介面與動畫設計 Skills，提供互動細節、動畫檢查、元件選擇和原型設計指引。
  - **適合你／怎麼用**：適合你請 Codex 製作小工具介面時使用；可先用 `prototype` 比較版本，再用設計或動畫 Skill 檢查細節。
  - [詳細說明](research-notes/emilkowalski--skills.md)
- **[mattpocock/skills](https://github.com/mattpocock/skills)** - Popular AI coding skills collection. (⭐ 263,348)
- **[andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills)** - Andrej Karpathy inspired AI skills. (⭐ 213,337)
- **[last30days-skill](https://github.com/mvanhorn/last30days-skill)** - Skill for recent work tracking. (⭐ 62,129)
- **[last30days-skill-cn](https://github.com/Jesseovo/last30days-skill-cn)** - Chinese version of last30days-skill. (⭐ 1,793)
- **[yao-meta-skill](https://github.com/yaojingang/yao-meta-skill)** - Meta skill for AI agents. (⭐ 2,617)
- **[sepia](https://github.com/Nanako0129/sepia)** - De-AI writing skill for agents. (⭐ 2,639)
  - **研究摘要**：這是給 AI Agent 的寫作 Skill，處理制式、冗長的 AI 文風，也提供專業文件與技術文章的寫作規則。
  - **適合你／怎麼用**：適合整理你的技術文件、Issue／PR 回覆與除錯紀錄；可先針對一篇草稿使用 Professional Writing 規則並人工核對事實。
  - [詳細說明](research-notes/Nanako0129--sepia.md)
- **[craft-skills](https://github.com/ZSeven-W/craft-skills)** - Research-backed, eval-driven skills for AI agents. (⭐ 154)
- **[SkillSpector](https://github.com/NVIDIA/SkillSpector)** - NVIDIA's skill evaluation tool. (⭐ 17,398)
- **[codex-keysmith](https://github.com/Jia-Ethan/codex-keysmith)** - Versioned Codex instruction deployment. (⭐ 4,501)
- **[aidlc-workflows](https://github.com/awslabs/aidlc-workflows)** - AI-Driven Life Cycle adaptive workflow steering. (⭐ 4,652)

### 其他 Agent 相關
- **[agentic-rag-for-dummies](https://github.com/GiovanniPasq/agentic-rag-for-dummies)** - Modular Agentic RAG built with LangGraph. (⭐ 4,172)
- **[CL4R1T4S](https://github.com/elder-plinius/CL4R1T4S)** - Agent framework. (⭐ 49,920)
- **[openhuman](https://github.com/tinyhumansai/openhuman)** - Open human-AI interaction framework. (⭐ 39,817)
- **[HermesOffice](https://github.com/criptogus/HermesOffice)** - AI-native office suite with Hermes Agent as the brain. (⭐ 578)
- **[openchamber](https://github.com/openchamber/openchamber)** - Agentic Development Environment based on OpenCode AI agent. (⭐ 9,921)
- **[gepa](https://github.com/gepa-ai/gepa)** - Optimize prompts, code, and more with AI-powered Reflective Optimization. (⭐ 6,599)
- **[llmfit](https://github.com/AlexsJones/llmfit)** - LLM fine-tuning toolkit. (⭐ 36,659)
- **[headroom](https://github.com/headroomlabs-ai/headroom)** - AI agent workspace. (⭐ 72,423)
- **[ruflo](https://github.com/ruvnet/ruflo)** - Agentic workflow system. (⭐ 72,600)
- **[superpowers](https://github.com/obra/superpowers)** - Agent superpowers framework. (⭐ 287,485)
- **[ponytail](https://github.com/DietrichGebert/ponytail)** - Agent coordination system. (⭐ 140,002)

---

## 📚 學習資源與教程

### AI 基礎
- **[generative-ai-for-beginners](https://github.com/microsoft/generative-ai-for-beginners)** - 21 Lessons, Get Started Building with Generative AI. (⭐ 119,863)
- **[Foundations-of-LLMs](https://github.com/ZJU-LLMs/Foundations-of-LLMs)** - A book for Learning the Foundations of LLMs. (⭐ 17,893)
- **[LLMs-from-scratch](https://github.com/rasbt/LLMs-from-scratch)** - Implement a ChatGPT-like LLM in PyTorch from scratch. (⭐ 105,076)
- **[dive-into-llms](https://github.com/Lordog/dive-into-llms)** - 《動手學大模型 Dive into LLMs》系列編程實踐教程。(⭐ 54,403)
- **[AI-For-Beginners](https://github.com/microsoft/AI-For-Beginners)** - 12 Weeks, 24 Lessons, AI for All! (⭐ 68,574)

### Agent 專業
- **[ai-agent-book](https://github.com/bojieli/ai-agent-book)** - 《深入理解 AI Agent：設計原理與工程實踐》開源主倉庫。(⭐ 47,959)
- **[awesome-agentic-ai-zh](https://github.com/WenyuChiou/awesome-agentic-ai-zh)** - Trilingual learning roadmap for agentic AI. (⭐ 7,034)
- **[agentic-design-patterns](https://github.com/xindoo/agentic-design-patterns)** - 谷歌 Agent 設計模式最佳中文版。(⭐ 8,020)
- **[learn-claude-code](https://github.com/shareAI-lab/learn-claude-code)** - Complete guide to learning Claude Code. (⭐ 76,948)
- **[ai-engineering-from-scratch](https://github.com/rohitg00/ai-engineering-from-scratch)** - AI Engineering fundamentals course. (⭐ 54,774)

### 自我提升
- **[the-craft-of-selfteaching](https://github.com/selfteaching/the-craft-of-selfteaching)** - One has no future if one couldn't teach themself. (⭐ 16,819)
- **[A-Programmers-Guide-to-English](https://github.com/yujiangshui/A-Programmers-Guide-to-English)** - 專為程序員編寫的英語學習指南。(⭐ 16,691)
- **[time-as-a-friend](https://github.com/xiaolai/time-as-a-friend)** - 《把時間當作朋友》。(⭐ 2,820)
- **[resources-to-become-a-great-engineering-leader](https://github.com/gregorojstersek/resources-to-become-a-great-engineering-leader)** - List of books, blogs, newsletters and people! (⭐ 7,643)
- **[FDE-the-Guidance-Book-of-Forward-Deployed-Engineer](https://github.com/xdash/FDE-the-Guidance-Book-of-Forward-Deployed-Engineer)** - FDE（前沿部署工程師）從零入門指南。(⭐ 4,724)

### 系統設計
- **[system-design-notes](https://github.com/liquidslr/system-design-notes)** - Notes of the book System Design Interview. (⭐ 20,018)

### 其他教程
- **[agents-from-scratch](https://github.com/langchain-ai/agents-from-scratch)** - Build an email assistant with human-in-the-loop and memory. (⭐ 2,225)
- **[rlhf-book-zh-tw](https://github.com/ai-twinkle/rlhf-book-zh-tw)** - 《Reinforcement Learning from Human Feedback》繁體中文全譯本。(⭐ 179)
- **[machine-learning-visualized](https://github.com/gavinkhung/machine-learning-visualized)** - ML algorithms implemented and derived from first-principles. (⭐ 1,964)
- **[ai-job-search](https://github.com/MadsLorentzen/ai-job-search)** - AI-powered job search platform. (⭐ 43,071)

---

## 🎨 設計與可視化工具

### 圖表和圖形
- **[lieflat-charts](https://github.com/larashero3-dotcom/lieflat-charts)** - Data visualization Skill, turning data into polished HTML charts. (⭐ 5,470)
- **[fireworks-tech-graph](https://github.com/yizhiyanhua-ai/fireworks-tech-graph)** - Generate production-quality SVG+PNG technical diagrams from natural language. (⭐ 11,432)
- **[ppt-master](https://github.com/hugohe3/ppt-master)** - AI turns documents into real, native PowerPoint decks. (⭐ 54,772)
  - **研究摘要**：這是讓 AI Agent 從文件、資料或主題規劃並產出可編輯 PowerPoint 的製作流程，目標是保留文字、形狀和圖表等原生物件。
  - **適合你／怎麼用**：適合把測試結果或技術報告整理成給主管看的簡報；先提供資料、聽眾與頁數，再於 PowerPoint 檢查內容和可編輯性。
  - [詳細說明](research-notes/hugohe3--ppt-master.md)
- **[awesome-gpt-image-2](https://github.com/freestylefly/awesome-gpt-image-2)** - GPT Image 提示詞與案例庫。(⭐ 32,221)

### 視覺內容
- **[handraw-style](https://github.com/yang0/handraw-style)** - 手繪風格編號畫廊與雙語提示詞 Skill。(⭐ 1,972)
- **[ian-xiaohei-illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations)** - 中文小黑怪誕正文配圖生成 Skill。(⭐ 11,722)
  - **研究摘要**：這是把文章轉成小黑風格插圖的 Agent Skill，包含選圖流程、風格規格、構圖範例與品質檢查。
  - **適合你／怎麼用**：對你更有價值的是它的 Skill 結構：可參考其按需讀取的知識檔與檢查步驟，設計自己的技術筆記插圖流程。
  - [詳細說明](research-notes/helloianneo--ian-xiaohei-illustrations.md)
- **[ip-as-logo-skill](https://github.com/s1dashu/ip-as-logo-skill)** - A compact Agent Skill for IP mascot logos. (⭐ 5,288)
- **[srt-whiteboard-animation](https://github.com/geeklee/srt-whiteboard-animation)** - SRT 字幕流式笔迹白板手繪動畫 skill。(⭐ 3,334)
- **[chinese-traditional-patterns](https://github.com/dososo/chinese-traditional-patterns)** - Chinese traditional patterns collection. (⭐ 299)

### 文檔和演示
- **[holo-card-studio](https://github.com/EverettFish/holo-card-studio)** - Blender card and interactive Three.js page generator. (⭐ 1,558)
- **[dashi-ppt-skill](https://github.com/chuspeeism/dashi-ppt-skill)** - Browser-editable presentations with exportable options. (⭐ 8,302)

---

## 🔍 RAG & 知識管理

### RAG 引擎
- **[ragflow](https://github.com/infiniflow/ragflow)** - Leading open-source RAG engine with Agent capabilities. (⭐ 90,810)
- **[LEANN](https://github.com/StarTrail-org/LEANN)** - RAG with 97% storage savings. (⭐ 12,941)

### 知識庫管理
- **[llm_wiki](https://github.com/nashsu/llm_wiki)** - Cross-platform desktop app that turns documents into organized knowledge base. (⭐ 19,632)
- **[obsidian-llm-wiki](https://github.com/GD4AI/obsidian-llm-wiki)** - Karpathy's LLM Wiki implementation plugin for Obsidian. (⭐ 626)
  - **研究摘要**：這是把 Karpathy LLM Wiki 工作方式帶進 Obsidian 的外掛，協助以 AI 整理和連結個人知識。
  - **適合你／怎麼用**：適合你現有的 Obsidian 筆記庫；可先在副本試用文件匯入、知識整理與引用回溯，再決定是否納入主要筆記流程。
  - [詳細說明](research-notes/GD4AI--obsidian-llm-wiki.md)
- **[Understand-Anything](https://github.com/Egonex-AI/Understand-Anything)** - Turn any code into interactive knowledge graph. (⭐ 83,035)
- **[knowledge-catalog](https://github.com/GoogleCloudPlatform/knowledge-catalog)** - Knowledge management catalog. (⭐ 9,214)

### 文檔處理
- **[MinerU](https://github.com/opendatalab/MinerU)** - Transforms complex documents into LLM-ready markdown/JSON. (⭐ 80,038)
- **[Unlimited-OCR](https://github.com/baidu/Unlimited-OCR)** - Unlimited OCR Works. (⭐ 25,717)
- **[Umi-OCR](https://github.com/hiroi-sora/Umi-OCR)** - OCR software, free and offline. (⭐ 47,340)
- **[PDFMathTranslate](https://github.com/PDFMathTranslate/PDFMathTranslate)** - PDF scientific paper translation with preserved formats. (⭐ 36,997)
- **[liteparse](https://github.com/run-llama/liteparse)** - Lightweight document parsing for LLMs. (⭐ 12,316)
  - **研究摘要**：這是可在本機執行的輕量文件解析工具，將 PDF 等文件轉成文字、Markdown 或結構化資料，供 LLM、RAG 或程式使用。
  - **適合你／怎麼用**：適合放在你文件整理與報告流程的前處理階段；先用代表性的 PDF 檢查段落、表格與來源位置是否保留。
  - [詳細說明](research-notes/run-llama--liteparse.md)
- **[opendataloader-pdf](https://github.com/opendataloader-project/opendataloader-pdf)** - PDF data loading tool. (⭐ 29,286)
- **[KillerPDF](https://github.com/SteveTheKiller/KillerPDF)** - Free and open-source PDF editor. (⭐ 3,864)
- **[ky-markdown-rebuilder](https://github.com/KyrieCheungYep/ky-markdown-rebuilder)** - Rebuild visually complex documents into Markdown. (⭐ 118)
- **[markitdown](https://github.com/microsoft/markitdown)** - Microsoft's Markdown conversion tool. (⭐ 184,691)

### 其他 RAG 相關
- **[AutoRAG](https://github.com/Marker-Inc-Korea/AutoRAG)** - AutoRAG: Now your agent can find anything in your computer. (⭐ 5,073)
- **[qiaomu-anything-to-notebooklm](https://github.com/joeseesun/qiaomu-anything-to-notebooklm)** - Multi-source content processor for NotebookLM. (⭐ 5,994)
- **[turbovec](https://github.com/RyanCodrai/turbovec)** - Vector index built on TurboQuant. (⭐ 17,193)

---

## 💻 開發工具與效率

### 代碼審查與質量
- **[open-code-review](https://github.com/alibaba/open-code-review)** - Fast, efficient code review tool with LLM Agent. (⭐ 30,647)
- **[spec-kit](https://github.com/github/spec-kit)** - Toolkit for Spec-Driven Development. (⭐ 137,255)
- **[ECC](https://github.com/affaan-m/ECC)** - Code quality assessment tool. (⭐ 259,793)

### 代碼理解
- **[codeflow](https://github.com/braedonsaunders/codeflow)** - Paste any GitHub URL → interactive architecture map. (⭐ 5,207)

### 內容提取與爬蟲
- **[crawl4ai](https://github.com/unclecode/crawl4ai)** - Open-source LLM Friendly Web Crawler & Scraper. (⭐ 83,663)
- **[Scrapling](https://github.com/D4Vinci/Scrapling)** - Advanced web scraping tool. (⭐ 81,343)
- **[instaloader](https://github.com/instaloader/instaloader)** - Download pictures and metadata from Instagram. (⭐ 13,387)
- **[TwitterMediaHarvest](https://github.com/EltonChou/TwitterMediaHarvest)** - Download media from Twitter. (⭐ 1,169)
- **[CloakBrowser](https://github.com/CloakHQ/CloakBrowser)** - Privacy-focused browser for web automation. (⭐ 31,497)

### 會議與記錄
- **[recensa](https://github.com/S40911120/recensa)** - Self-hosted web viewer for Claude Code session transcripts. (⭐ 72)
- **[ownscribe](https://github.com/nczz/ownscribe)** - Local-first meeting transcription and summarization CLI. (⭐ 178)

### 編輯與排版
- **[markdown-online-editor](https://github.com/nicejade/markdown-online-editor)** - Online Markdown editor with diagram support. (⭐ 3,971)
- **[commentflow](https://github.com/sysprog21/commentflow)** - Reflow comments in C, C++, Rust, POSIX shell, and GAS assembly. (⭐ 27)

---

## 🎬 視頻/音頻/內容生成

- **[OpenMontage](https://github.com/calesthio/OpenMontage)** - World's first open-source, agentic video production system. (⭐ 59,477)
- **[autoclip](https://github.com/zhouxiaoka/autoclip)** - AI-powered video clipping and highlight generation. (⭐ 7,340)
- **[Echo-Loop](https://github.com/echo-loop/Echo-Loop)** - Scientific, efficient AI English listening and speaking training App. (⭐ 3,546)
- **[OpenCut](https://github.com/OpenCut-app/OpenCut)** - The open-source CapCut alternative. (⭐ 89,580)
- **[VidBee](https://github.com/nexmoe/VidBee)** - Video processing and generation tool. (⭐ 10,647)
- **[wenyi](https://github.com/BigDawnGhost/wenyi)** - Bringing literature into your language. (⭐ 2,602)

---

## 💰 金融與投資

- **[qlib](https://github.com/microsoft/qlib)** - AI-oriented Quant investment platform. (⭐ 48,606)
- **[wealth-tracker](https://github.com/nicejade/wealth-tracker)** - Personal asset analysis application with AI advice. (⭐ 905)
- **[Financial_freedom](https://github.com/codeman008/Financial_freedom)** - Technical guide to making money and investing. (⭐ 3,823)
- **[FinceptTerminal](https://github.com/Fincept-Corporation/FinceptTerminal)** - Modern finance application with advanced market analytics. (⭐ 31,690)

---

## 📖 資源合集

- **[awesome](https://github.com/sindresorhus/awesome)** - Awesome lists about all kinds of interesting topics. (⭐ 506,592)
- **[HelloGitHub](https://github.com/521xueweihan/HelloGitHub)** - Share interesting, entry-level open source projects on GitHub. (⭐ 176,872)
- **[the-book-of-secret-knowledge](https://github.com/trimstray/the-book-of-secret-knowledge)** - A collection of inspiring lists and cheatsheets. (⭐ 244,092)
- **[awesome-llm-apps](https://github.com/Shubhamsaboo/awesome-llm-apps)** - 100+ AI Agents, Agent Skills and RAG Apps. (⭐ 138,459)
- **[awesome-vibe-coding](https://github.com/filipecalegario/awesome-vibe-coding)** - Awesome vibe coding resources. (⭐ 5,257)
- **[vibe-coding-cn](https://github.com/tradecatlabs/vibe-coding-cn)** - Chinese vibe coding guide. (⭐ 16,251)

---

## 🔧 其他實用工具

### 系統與應用
- **[syncthing](https://github.com/syncthing/syncthing)** - Open Source Continuous File Synchronization. (⭐ 88,644)
- **[harness](https://github.com/harness/harness)** - Continuous delivery platform. (⭐ 38,366)
- **[harness-engineering](https://github.com/deusyu/harness-engineering)** - Harness engineering practices. (⭐ 5,942)
- **[self-harness](https://github.com/datawhalechina/self-harness)** - Self-learning harness framework. (⭐ 254)
- **[compound-engineering-plugin](https://github.com/EveryInc/compound-engineering-plugin)** - Compound engineering plugin. (⭐ 25,103)
- **[planning-with-files](https://github.com/OthmanAdi/planning-with-files)** - Planning tool with file integration. (⭐ 26,934)
- **[career-ops](https://github.com/career-ops-hq/career-ops)** - Career operations management platform. (⭐ 71,795)

### 簡歷與個人品牌
- **[magic-resume](https://github.com/JOYCEQL/magic-resume)** - Free online AI resume editor. (⭐ 10,571)

### 其他
- **[airi](https://github.com/moeru-ai/airi)** - Self hosted, you-owned Grok Companion. (⭐ 49,181)
- **[up](https://github.com/byoungd/up)** - Terminal application. (⭐ 62,840)
- **[lecture-to-notes](https://github.com/drpwchen/lecture-to-notes)** - Lecture recordings → structured grounded notes. (⭐ 103)
- **[niamos](https://github.com/pricklywiggles/niamos)** - Utility tool. (⭐ 192)
- **[whichllm](https://github.com/Andyyyy64/whichllm)** - Find the local LLM that actually runs best on your hardware. (⭐ 6,644)
- **[egos-2000](https://github.com/yhzhang0128/egos-2000)** - Envision a future where everyone can read all the code of an educational OS. (⭐ 3,616)
- **[Horizon](https://github.com/Thysrael/Horizon)** - Development environment. (⭐ 9,368)
- **[heretic](https://github.com/p-e-w/heretic)** - Utility tool. (⭐ 31,552)
- **[BD2-L2D-Viewer](https://github.com/Jelosus2/BD2-L2D-Viewer)** - Viewer tool. (⭐ 494)

---

## 📊 統計數據

- **Total Stars**: 150+ repositories
- **Highest Stars**: awesome (506,592 ⭐)
- **Main Categories**: AI/Agent (40%), Learning Resources (15%), Design & Visualization (15%), RAG & Knowledge (10%), Tools (20%)

---

## 📝 說明

此列表是根據個人 GitHub Stars 進行分類整理。分類基於每個項目的主要功能和應用領域。

如需更新或有建議，歡迎提 Issue 或 PR！

**最後更新**: 2026-09-16
