# machine-learning-visualized｜GitHub 專案導覽

> 來源：[專案 README](https://github.com/gavinkhung/machine-learning-visualized/blob/HEAD/README.md)；查閱日期：2026-09-16。

## 1. 這是什麼？

這是以 Jupyter Book 呈現的機器學習教材，展示模型訓練時權重與損失如何變化，也提供 Marimo 互動 Notebook。README 特別說明：這個倉庫主要負責網站組態與建置，各演算法的 Notebook 位於其他獨立倉庫，並非都直接收在這裡。主題包括神經網路、邏輯迴歸、感知器、PCA、K-means 與梯度下降。

## 2. 對我有什麼用？

你若需要把模型評估或訓練概念講給同事聽，視覺化可比公式更容易討論；也能幫你判斷「模型是否真的學到規律」。對目前以自動化測試與報告為主的工作，這比較偏補充學習材料，不是即插即用的製圖工具。

## 3. 使用情境

例如讀邏輯迴歸或梯度下降範例，觀察改變權重如何影響損失與決策，再思考如果用模型分類測試失敗，如何避免只看最終準確率。可將圖像與自己的資料案例配對，寫進 Obsidian 當概念筆記；不應把教學圖直接當作生產資料的結果。

## 4. 我要怎麼用？

最快方式是開 README 指向的線上 Jupyter Book 或各演算法倉庫。若要本機建站，先按 Usage 執行下載 Notebook 的 shell 腳本，再用 `pip install -U jupyter-book` 或 README 的 Docker Compose／Docker 選項建置，最後開生成的書站。三種建置介面擇一即可；Notebook 本體由其他倉庫取得，先確認腳本下載結果。

## 5. 值不值得研究？

可以先收藏，以後可能用到：適合學習或解釋機器學習原理；目前工作沒有明確模型訓練需求時優先度不高。
