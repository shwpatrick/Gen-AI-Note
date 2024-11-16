# Operationalizing Generative AI on Vertex AI using MLOps

### 什麼是 DevOps 和 MLOps

- DevOps 是⼀種軟體⼯程⽅法，旨在彌合開發 (Dev) 和營運 (Ops) 之間的差距

- MLOps 以 DevOps 原則為基礎，旨在解決快速可靠地操作機器學習系統的獨特挑戰

## 使用 fundation models (FM)

-  使用FM作為微調模型的基礎
- FM通常為multi-purpose tools -> 可以進行微調
- 不是像kaggler model 通常只針對單一任務
### 效能評估關注點

- 品質
- 延遲和吞吐量
- 開發與維運時間
- 使用成本
- 合法性

### 快速工程的迭代步驟

1. 提示：模型定義的原則，需要足夠精準完備
2. 評估：評估效果
### vertax AI 提供內容

 vertax model garden - FM集合
 automatic sidebyside(Auto sxs) - 引入其他LLM去評分

## 如何為Gen AI的產出評分

- 人工評價
- LLM評分系統

## 如何單獨評價特定步驟的效果而非整體

monitoring   
設定每一個步驟的程度  
vertex AI 有工具可以檢測 偏離程度  
評分系統在多model時要分別對應選擇套用  

## 實作注意點

- 耗能 GPU TPU
- latency scalability
- 雲端運算
- Vertex AI endpoint ，可以將你的模型產生API給其他端口使用
- safety - citation checking vertex AI 工具可以檢查著作權
- bias generating harmful content - safety score tool
