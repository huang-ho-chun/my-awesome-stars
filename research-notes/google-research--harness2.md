# Harness²｜GitHub 專案導覽

> 來源：[google-research/harness2](https://github.com/google-research/harness2) README；查閱日期：2026-10-19。

## 1. 這是什麼？

Harness² 是 Google Research 發布的 **Agent Harness 改進研究框架**。模型權重保持固定，改的是模型周邊的 system prompt、guardrails、memory、工具指引、subagent、skills、scripts 與 plugins。它讓 Agent 對手上的任務提出候選改法、實際試跑、根據結果整合；也會保存已採用的改法與證據，供後續任務參考。

它適合有可重複測試任務的人研究「Agent 工作方式是否真的變好」，並非安裝後就能自動改善日常聊天的工具。

## 2. 對我有什麼用？

你在整理 GitHub 專案、Codex Skills 與自動化流程時，可以借用它的核心方法：先定義完成標準，再讓不同指引或工具配置處理相同任務，檢查實際成果，而不是只憑主觀感覺修改 Prompt。

例如，若你累積了一批附有可信參考答案的「GitHub 專案導覽」案例，可以比較不同導覽 Skill 是否更能抓到用途、使用門檻及適用情境。若還沒有穩定的測試案例，先研究方法即可，直接導入框架的收益有限。

## 3. 使用情境

- **Agent 研究者**：在 JobBench、LAB 或 WorkBuddy-Bench 上比較 Harness 改法。
- **Agent 開發者**：對工具說明、記憶與 Skill 做可驗證的調整，觀察是否改善真實任務。
- **個人工作流程**：參考「提出改法 → 試跑 → 留下證據」流程，手動改進自己的 Agent；不一定要部署 Harness²。

## 4. 我要怎麼用？

若只是想理解，先看 README 的 Harness components 與 Experiments，再試官方不需模型憑證的本機 demo。README 指定 Linux、Python 3.12、uv；在 repo 根目錄建立環境、安裝 `.[render]`，執行 `harness2-demo --output runs/demo --k 2`，就能看到兩種遞迴模式的示範結果。

要跑模型 Benchmark，還需 Node.js 20+、Google Cloud CLI、模型與 Vertex AI 設定；部分 Benchmark 需要額外軟體，執行也會產生 API 費用。先選一個 Benchmark、一個任務小範圍試跑，再用配套的 judge/report 檢查成果。專案也提供 Codex executor，但文件指出其執行時沙箱會關閉，應先看清執行環境與網路存取設定。

## 5. 值不值得研究？

**有特定情境才有用。** 對你最有價值的是「用任務證據改善 Agent」的方法；若尚未準備可評估的案例與執行預算，先收藏、閱讀 demo，比直接投入完整實驗合適。
