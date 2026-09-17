# 🌟 My Awesome Stars Collection

個人精選 GitHub Stars，按分類整理。涵蓋 AI Agent、LLM、數據可視化、知識管理、開發工具等多個領域。

**Last Updated**: 2026-09-17

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
- **[Langflow](https://github.com/langflow-ai/langflow)** - 用圖形介面串接模型、資料與工具，建立可部署的 AI Agent 工作流程。 (⭐ 154,880)
  - [詳細說明](research-notes/langflow-ai--langflow.md)
- **[DSPy](https://github.com/stanfordnlp/dspy)** - 以 Python 定義並評估 LLM 流程，再最佳化提示與模型設定。 (⭐ 38,065)
  - [詳細說明](research-notes/stanfordnlp--dspy.md)
- **[SkillOpt](https://github.com/microsoft/SkillOpt)** - 以任務驗證結果改善 Agent Skill 指引的工具與研究框架。 (⭐ 17,154)
  - **研究摘要**：這是改善 AI Agent Skill 的文字優化工具，從任務成敗找出修改方向，再用驗證任務檢查是否真的變好。
  - **適合你／怎麼用**：適合用來改進你反覆使用的 Codex Skills 與工作規範；可先看從歷史工作紀錄學習的 SkillOpt-Sleep，再決定是否導入完整訓練流程。
  - [詳細說明](research-notes/microsoft--SkillOpt.md)
- **[OpenMAIC](https://github.com/THU-MAIC/OpenMAIC)** - 將主題或資料變成多 Agent 互動課堂的課程生成系統。 (⭐ 37,318)
  - [詳細說明](research-notes/THU-MAIC--OpenMAIC.md)
- **[Hermes Agent](https://github.com/NousResearch/hermes-agent)** - 整合工具、記憶與排程，可在終端或訊息平台使用的個人 Agent。 (⭐ 246,062)
  - [詳細說明](research-notes/NousResearch--hermes-agent.md)
- **[Hermes Desktop](https://github.com/fathah/hermes-desktop)** - 管理 Hermes Agent 聊天、設定與工作紀錄的社群桌面介面。 (⭐ 14,231)
  - [詳細說明](research-notes/fathah--hermes-desktop.md)

### Agent 工具
- **[context-mode](https://github.com/mksglu/context-mode)** - 縮減 Coding Agent 工具輸出占用的上下文，保留可查詢內容。 (⭐ 23,185)
  - [詳細說明](research-notes/mksglu--context-mode.md)
- **[i-have-adhd](https://github.com/ayghri/i-have-adhd)** - 讓 Coding Agent 先說重點與下一步的輸出風格 Skill。 (⭐ 46,685)
  - **研究摘要**：這是調整 Coding Agent 回答方式的 Skill：先給下一步、清楚編號並保留目前進度，避免重點埋在長篇說明中。
  - **適合你／怎麼用**：適合你與 Codex 多輪除錯時使用；可依自己的偏好改寫規則，讓每輪都交代已確認事項與下一個動作。
  - [詳細說明](research-notes/ayghri--i-have-adhd.md)
- **[GitNexus](https://github.com/abhigyanpatwari/GitNexus)** - 為程式庫建立關係索引，查詢符號、呼叫路徑與修改影響。 (⭐ 47,380)
  - [詳細說明](research-notes/abhigyanpatwari--GitNexus.md)
- **[Agent-Reach](https://github.com/Panniantong/Agent-Reach)** - 替 Agent 設定並檢查多平台網路資料存取能力。 (⭐ 82,337)
  - [詳細說明](research-notes/Panniantong--Agent-Reach.md)
- **[codegraph](https://github.com/colbymchenry/codegraph)** - 建立程式碼呼叫與相依關係索引，供 Coding Agent 查詢。 (⭐ 71,127)
  - **研究摘要**：這是替程式庫建立符號、呼叫與相依關係索引的工具，讓 Coding Agent 能查詢程式碼關係及修改影響範圍。
  - **適合你／怎麼用**：適合你處理跨多個檔案的報告流程或測試工具時，先索引專案，再請 Agent 查函式呼叫路徑與相關模組。
  - [詳細說明](research-notes/colbymchenry--codegraph.md)
- **[context-hub](https://github.com/andrewyng/context-hub)** - 提供 Coding Agent 可查閱、可註記的版本化 API 文件。 (⭐ 13,981)
  - [詳細說明](research-notes/andrewyng--context-hub.md)

### 多模態
- **[CosyVoice](https://github.com/QwenAudio/CosyVoice)** - 提供多語言語音生成與參考聲音複製的模型專案。 (⭐ 23,641)
  - [詳細說明](research-notes/QwenAudio--CosyVoice.md)
- **[Seedance 2.0](https://github.com/Emily2040/seedance-2.0)** - 規劃影片分鏡與參考素材的 Agent Skill，生成需外部服務。 (⭐ 7,342)
  - [詳細說明](research-notes/Emily2040--seedance-2.0.md)
- **[claude-video](https://github.com/bradautomates/claude-video)** - 讓 Coding Agent 結合字幕與影格分析影片內容的 Skill。 (⭐ 17,268)
  - [詳細說明](research-notes/bradautomates--claude-video.md)
- **[book-to-skill](https://github.com/virgiliojr94/book-to-skill)** - 將書籍與文件整理成可按需查閱的 Agent Skill。 (⭐ 30,879)
  - **研究摘要**：這是把技術書或文件整理成可重複使用的 Agent Skill 的工具，將核心指引與詳細章節分開供 Agent 按需讀取。
  - **適合你／怎麼用**：適合把常查的 Linux、效能或軟體架構資料變成 Codex 的參考 Skill；先確認產出的索引與內容，再用實際問題測試。
  - [詳細說明](research-notes/virgiliojr94--book-to-skill.md)
- **[VoxCPM](https://github.com/OpenBMB/VoxCPM)** - 支援多語言朗讀、聲音設計與參考聲音複製的語音模型。 (⭐ 37,639)
  - [詳細說明](research-notes/OpenBMB--VoxCPM.md)
- **[VibeVoice](https://github.com/microsoft/VibeVoice)** - 涵蓋長音訊辨識、多人語音與串流合成的語音 AI 專案。 (⭐ 54,336)
  - [詳細說明](research-notes/microsoft--VibeVoice.md)

### Agent Skills
- **[archify](https://github.com/tt-a1i/archify)** - 將程式碼或系統描述轉成可檢查的互動架構圖。 (⭐ 64,422)
  - [詳細說明](research-notes/tt-a1i--archify.md)
- **[diagram-design](https://github.com/cathrynlavery/diagram-design)** - 提供多種圖解類型與視覺規則的 Agent Skill。 (⭐ 40,413)
  - [詳細說明](research-notes/cathrynlavery--diagram-design.md)
- **[effective-html](https://github.com/plannotator/effective-html)** - 引導 Coding Agent 製作 HTML 圖解、線框圖與互動原型。 (⭐ 3,190)
  - **研究摘要**：這是一組教 Coding Agent 製作 HTML 資訊成品的 Skills，涵蓋圖解、線框圖、可操作原型與視覺化計畫。
  - **適合你／怎麼用**：適合把你的測試流程、報告架構或方案比較做成可開啟的頁面；需要看流程時可從 `html-diagram` 開始。
  - [詳細說明](research-notes/plannotator--effective-html.md)
- **[flint-chart](https://github.com/microsoft/flint-chart)** - 讓 Agent 描述資料意義與圖表需求，再產生可讀圖表。 (⭐ 4,215)
  - **研究摘要**：這是供 AI Agent 使用的圖表描述與生成層，讓 Agent 指定資料意義和圖表需求，再處理座標軸、標籤與版面等細節。
  - **適合你／怎麼用**：適合把測試數據接到自動報告流程，產生可閱讀的效能比較圖；先用一份 CSV 試作並核對圖表與原始數值。
  - [詳細說明](research-notes/microsoft--flint-chart.md)
- **[cangjie-skill](https://github.com/kangarooking/cangjie-skill)** - 從書籍、影片與播客萃取方法，轉成可呼叫的 Agent Skills。 (⭐ 10,145)
  - [詳細說明](research-notes/kangarooking--cangjie-skill.md)
- **[dashi-ppt-skill](https://github.com/chuspeeism/dashi-ppt-skill)** - 讓 Agent 產生可在瀏覽器編輯、可輸出 PPTX 的簡報。 (⭐ 8,302)
  - [詳細說明](research-notes/chuspeeism--dashi-ppt-skill.md)
- **[holo-card-studio](https://github.com/EverettFish/holo-card-studio)** - 用 Codex Skill 製作全息卡牌、Blender 工程與互動頁面。 (⭐ 1,558)
  - [詳細說明](research-notes/EverettFish--holo-card-studio.md)
- **[skills](https://github.com/emilkowalski/skills)** - 協助 Coding Agent 改善介面設計、動畫與互動細節的 Skills。 (⭐ 38,203)
  - **研究摘要**：這是一組給 Coding Agent 的介面與動畫設計 Skills，提供互動細節、動畫檢查、元件選擇和原型設計指引。
  - **適合你／怎麼用**：適合你請 Codex 製作小工具介面時使用；可先用 `prototype` 比較版本，再用設計或動畫 Skill 檢查細節。
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
  - **研究摘要**：這是給 AI Agent 的寫作 Skill，處理制式、冗長的 AI 文風，也提供專業文件與技術文章的寫作規則。
  - **適合你／怎麼用**：適合整理你的技術文件、Issue／PR 回覆與除錯紀錄；可先針對一篇草稿使用 Professional Writing 規則並人工核對事實。
  - [詳細說明](research-notes/Nanako0129--sepia.md)
- **[craft-skills](https://github.com/ZSeven-W/craft-skills)** - 以研究資料與評測結果設計的 Agent Skills 集合。 (⭐ 154)
  - [詳細說明](research-notes/ZSeven-W--craft-skills.md)
- **[SkillSpector](https://github.com/NVIDIA/SkillSpector)** - 在安裝前掃描 Agent Skills 潛在安全風險的工具。 (⭐ 17,398)
  - [詳細說明](research-notes/NVIDIA--SkillSpector.md)
- **[codex-keysmith](https://github.com/Jia-Ethan/codex-keysmith)** - 以版本化設定管理 Codex 指令與 hooks 的部署。 (⭐ 4,501)
  - [詳細說明](research-notes/Jia-Ethan--codex-keysmith.md)
- **[aidlc-workflows](https://github.com/awslabs/aidlc-workflows)** - 替多種 Coding Agent 提供結構化開發流程的範本。 (⭐ 4,652)
  - [詳細說明](research-notes/awslabs--aidlc-workflows.md)

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
- **[ai-agent-book](https://github.com/bojieli/ai-agent-book)** - 從 Agent 設計原理到工程實作的中文開源書與實驗。 (⭐ 47,959)
  - [詳細說明](research-notes/bojieli--ai-agent-book.md)
- **[awesome-agentic-ai-zh](https://github.com/WenyuChiou/awesome-agentic-ai-zh)** - 繁體中文 Agent 學習路線圖，含工具使用與建構者路線。 (⭐ 7,034)
  - [詳細說明](research-notes/WenyuChiou--awesome-agentic-ai-zh.md)
- **[agentic-design-patterns](https://github.com/xindoo/agentic-design-patterns)** - 介紹 21 種 Agent 設計模式的中文翻譯讀物。 (⭐ 8,020)
  - [詳細說明](research-notes/xindoo--agentic-design-patterns.md)
- **[learn-claude-code](https://github.com/shareAI-lab/learn-claude-code)** - 逐課拆解 Coding Agent 的工具、權限、記憶與工作流程。 (⭐ 76,948)
  - [詳細說明](research-notes/shareAI-lab--learn-claude-code.md)
- **[ai-engineering-from-scratch](https://github.com/rohitg00/ai-engineering-from-scratch)** - 從機器學習到 LLM、Agent 與部署的分階段自學課程。 (⭐ 54,774)
  - [詳細說明](research-notes/rohitg00--ai-engineering-from-scratch.md)

### 自我提升
- **[the-craft-of-selfteaching](https://github.com/selfteaching/the-craft-of-selfteaching)** - 用 Python 與寫作練習建立自學能力的開放教材。 (⭐ 16,819)
  - [詳細說明](research-notes/selfteaching--the-craft-of-selfteaching.md)
- **[A-Programmers-Guide-to-English](https://github.com/yujiangshui/A-Programmers-Guide-to-English)** - 面向程式設計者的中文英語學習方法與資源指南。 (⭐ 16,691)
  - [詳細說明](research-notes/yujiangshui--A-Programmers-Guide-to-English.md)
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
- **[lieflat-charts](https://github.com/larashero3-dotcom/lieflat-charts)** - 用 Agent Skill 把資料轉成 HTML 圖表或視覺報告。 (⭐ 5,470)
  - [詳細說明](research-notes/larashero3-dotcom--lieflat-charts.md)
- **[fireworks-tech-graph](https://github.com/yizhiyanhua-ai/fireworks-tech-graph)** - 依文字描述產生 SVG、PNG 架構圖與技術流程圖。 (⭐ 11,432)
  - [詳細說明](research-notes/yizhiyanhua-ai--fireworks-tech-graph.md)
- **[ppt-master](https://github.com/hugohe3/ppt-master)** - 讓 AI Agent 從文件製作可在 PowerPoint 編輯的簡報。 (⭐ 54,772)
  - **研究摘要**：這是讓 AI Agent 從文件、資料或主題規劃並產出可編輯 PowerPoint 的製作流程，目標是保留文字、形狀和圖表等原生物件。
  - **適合你／怎麼用**：適合把測試結果或技術報告整理成給主管看的簡報；先提供資料、聽眾與頁數，再於 PowerPoint 檢查內容和可編輯性。
  - [詳細說明](research-notes/hugohe3--ppt-master.md)
- **[awesome-gpt-image-2](https://github.com/freestylefly/awesome-gpt-image-2)** - 提供影像提示詞、案例與模板的資源庫。 (⭐ 32,221)
  - [詳細說明](research-notes/freestylefly--awesome-gpt-image-2.md)

### 視覺內容
- **[handraw-style](https://github.com/yang0/handraw-style)** - 用編號畫廊挑選手繪風格並產生對應提示詞。 (⭐ 1,972)
  - [詳細說明](research-notes/yang0--handraw-style.md)
- **[ian-xiaohei-illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations)** - 把中文文章內容轉成「小黑」風格正文插圖的 Skill。 (⭐ 11,722)
  - **研究摘要**：這是把文章轉成小黑風格插圖的 Agent Skill，包含選圖流程、風格規格、構圖範例與品質檢查。
  - **適合你／怎麼用**：對你更有價值的是它的 Skill 結構：可參考其按需讀取的知識檔與檢查步驟，設計自己的技術筆記插圖流程。
  - [詳細說明](research-notes/helloianneo--ian-xiaohei-illustrations.md)
- **[ip-as-logo-skill](https://github.com/s1dashu/ip-as-logo-skill)** - 協助 Agent 設計簡潔吉祥物 Logo 的 Skill。 (⭐ 5,288)
  - [詳細說明](research-notes/s1dashu--ip-as-logo-skill.md)
- **[srt-whiteboard-animation](https://github.com/geeklee/srt-whiteboard-animation)** - 依 SRT 字幕製作分鏡與白板手繪動畫的 Skill。 (⭐ 3,334)
  - [詳細說明](research-notes/geeklee--srt-whiteboard-animation.md)
- **[chinese-traditional-patterns](https://github.com/dososo/chinese-traditional-patterns)** - 提供傳統紋樣圖錄、寓意與應用資料的素材庫。 (⭐ 299)
  - [詳細說明](research-notes/dososo--chinese-traditional-patterns.md)

### 文檔和演示
- **[holo-card-studio](https://github.com/EverettFish/holo-card-studio)** - 用 Codex Skill 製作全息卡牌、Blender 工程與互動頁面。 (⭐ 1,558)
  - [詳細說明](research-notes/EverettFish--holo-card-studio.md)
- **[dashi-ppt-skill](https://github.com/chuspeeism/dashi-ppt-skill)** - 讓 Agent 產生可在瀏覽器編輯、可輸出 PPTX 的簡報。 (⭐ 8,302)
  - [詳細說明](research-notes/chuspeeism--dashi-ppt-skill.md)

---

## 🔍 RAG & 知識管理

### RAG 引擎
- **[ragflow](https://github.com/infiniflow/ragflow)** - 可自架的 RAG 問答平台，整合文件解析、檢索與引用。 (⭐ 90,810)
  - [詳細說明](research-notes/infiniflow--ragflow.md)
- **[LEANN](https://github.com/StarTrail-org/LEANN)** - 節省索引儲存空間的本機向量檢索與個人 RAG 工具。 (⭐ 12,941)
  - [詳細說明](research-notes/StarTrail-org--LEANN.md)

### 知識庫管理
- **[llm_wiki](https://github.com/nashsu/llm_wiki)** - 匯入文件並持續建立連結與知識圖譜的桌面知識庫。 (⭐ 19,632)
  - [詳細說明](research-notes/nashsu--llm_wiki.md)
- **[obsidian-llm-wiki](https://github.com/GD4AI/obsidian-llm-wiki)** - 在 Obsidian 中用 AI 建立來源、概念頁與筆記連結的外掛。 (⭐ 626)
  - **研究摘要**：這是把 Karpathy LLM Wiki 工作方式帶進 Obsidian 的外掛，協助以 AI 整理和連結個人知識。
  - **適合你／怎麼用**：適合你現有的 Obsidian 筆記庫；可先在副本試用文件匯入、知識整理與引用回溯，再決定是否納入主要筆記流程。
  - [詳細說明](research-notes/GD4AI--obsidian-llm-wiki.md)
- **[Understand-Anything](https://github.com/Egonex-AI/Understand-Anything)** - 把程式庫轉成互動知識圖，輔助理解依賴與變更影響。 (⭐ 83,035)
  - [詳細說明](research-notes/Egonex-AI--Understand-Anything.md)
- **[knowledge-catalog](https://github.com/GoogleCloudPlatform/knowledge-catalog)** - 展示 Google Cloud 資料目錄工具、Agent 與範例的倉庫。 (⭐ 9,214)
  - [詳細說明](research-notes/GoogleCloudPlatform--knowledge-catalog.md)

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
  - **研究摘要**：這是可在本機執行的輕量文件解析工具，將 PDF 等文件轉成文字、Markdown 或結構化資料，供 LLM、RAG 或程式使用。
  - **適合你／怎麼用**：適合放在你文件整理與報告流程的前處理階段；先用代表性的 PDF 檢查段落、表格與來源位置是否保留。
  - [詳細說明](research-notes/run-llama--liteparse.md)
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
- **[codeflow](https://github.com/braedonsaunders/codeflow)** - 貼上 GitHub 網址即可查看程式依賴與影響範圍的架構圖。 (⭐ 5,207)
  - [詳細說明](research-notes/braedonsaunders--codeflow.md)

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

- **[OpenMontage](https://github.com/calesthio/OpenMontage)** - 用 AI Agent 規劃鏡頭、素材與剪輯的開源影片製作流程。 (⭐ 59,477)
  - [詳細說明](research-notes/calesthio--OpenMontage.md)
- **[autoclip](https://github.com/zhouxiaoka/autoclip)** - 下載、切片並組合影音精華的 AI 輔助平台。 (⭐ 7,340)
  - [詳細說明](research-notes/zhouxiaoka--autoclip.md)
- **[Echo-Loop](https://github.com/echo-loop/Echo-Loop)** - 以精聽、跟讀、復述與複習練習英語聽說的 App。 (⭐ 3,546)
  - [詳細說明](research-notes/echo-loop--Echo-Loop.md)
- **[OpenCut](https://github.com/OpenCut-app/OpenCut)** - 開源影片編輯器；新版本重寫中，目前可用 Classic 版。 (⭐ 89,580)
  - [詳細說明](research-notes/OpenCut-app--OpenCut.md)
- **[VidBee](https://github.com/nexmoe/VidBee)** - 提供影音下載、RSS 追蹤與本機語音轉錄的應用程式。 (⭐ 10,647)
  - [詳細說明](research-notes/nexmoe--VidBee.md)
- **[wenyi](https://github.com/BigDawnGhost/wenyi)** - 維護術語與全書脈絡的長篇書籍 AI 翻譯工具。 (⭐ 2,602)
  - [詳細說明](research-notes/BigDawnGhost--wenyi.md)

---

## 💰 金融與投資

- **[qlib](https://github.com/microsoft/qlib)** - 涵蓋資料準備、模型訓練與回測的量化投資研究平台。 (⭐ 48,606)
  - [詳細說明](research-notes/microsoft--qlib.md)
- **[wealth-tracker](https://github.com/nicejade/wealth-tracker)** - 記錄、分析個人資產並提供 AI 解讀的應用程式。 (⭐ 905)
  - [詳細說明](research-notes/nicejade--wealth-tracker.md)
- **[Financial_freedom](https://github.com/codeman008/Financial_freedom)** - 彙整理財與投資書籍、工具和社群的資源清單。 (⭐ 3,823)
  - [詳細說明](research-notes/codeman008--Financial_freedom.md)
- **[FinceptTerminal](https://github.com/Fincept-Corporation/FinceptTerminal)** - 提供市場資料、投資研究與分析介面的桌面金融終端。 (⭐ 31,690)
  - [詳細說明](research-notes/Fincept-Corporation--FinceptTerminal.md)

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

---

## 🔧 其他實用工具

### 系統與應用
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

### 簡歷與個人品牌
- **[magic-resume](https://github.com/JOYCEQL/magic-resume)** - 提供即時預覽、主題與 PDF 匯出的開源履歷編輯器。 (⭐ 10,571)
  - [詳細說明](research-notes/JOYCEQL--magic-resume.md)

### 其他
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

---

## 📊 統計數據

- **Total Stars**: 150+ repositories
- **Highest Stars**: awesome (506,592 ⭐)
- **Main Categories**: AI/Agent (40%), Learning Resources (15%), Design & Visualization (15%), RAG & Knowledge (10%), Tools (20%)

---

## 📝 說明

此列表是根據個人 GitHub Stars 進行分類整理。分類基於每個項目的主要功能和應用領域。

如需更新或有建議，歡迎提 Issue 或 PR！

**最後更新**: 2026-09-17
