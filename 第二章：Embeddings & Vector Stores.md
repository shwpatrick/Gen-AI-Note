[程式碼實作參考：檢索強化生成(RAG)-在Prompt中加入資料庫](https://www.kaggle.com/code/markishere/day-2-document-q-a-with-rag)
[程式碼實作參考：檢索資料與資料庫的相似性比對](https://www.kaggle.com/code/markishere/day-2-embeddings-and-similarity-scores)
[程式碼是做參考：透過嵌入資料庫實現新聞分類器](https://www.kaggle.com/code/markishere/day-2-classifying-embeddings-with-keras) 

## 嵌入在大型語言模型 (LLM) 的應用

嵌入技術在 LLM 中起到核心作用，幫助模型理解和生成更準確的語意表達，適用於各類語意搜尋、問答和生成任務。  
概念從Prompt延伸，我們既然可以從Prompt優化回覆，  
自然可以透過將特定資料傳給Prompt，強化LLM的能力。  

## 關鍵應用：

檢索系統 (Retrieval System)：利用向量表示來更精確地檢索資料。  
推薦系統 (Recommendation System)：幫助預測用戶興趣。

## 嵌入的應用領域
  
檢索：利用嵌入來進行語意搜尋，而非僅依賴字面搜尋。  
推薦：基於嵌入來識別相似的內容，以個性化推薦結果。  

## 各種嵌入類型

文字嵌入 (Text Embedding)：將文本轉換成向量表示，常用於自然語言處理 (NLP)。  
TF-IDF：傳統的文本嵌入方法，基於詞頻進行向量化。  

影像嵌入 (Image Embedding)：利用卷積神經網絡 (CNN) 提取圖像特徵，將其轉換為向量表示。  

多模態嵌入 (Multimodal Embedding)：將多種形式的數據（例如圖像和文本）結合為統一的向量表示，讓模型能夠同時理解不同數據來源。  
Vertex AI：Google 的多模態平台，用於處理和訓練多模態模型。  

## 向量搜尋 (Vector Search)

意圖搜尋：基於語意進行搜尋，而非字面相似度，提升搜尋的準確性和相關性。  

## 資料量與維度問題

大量資料情況：當資料量過大時，提升搜尋速度和效率變得至關重要。  

### 低維資料：

最近鄰搜尋 (Nearest Neighbor Search) 和 近似最近鄰搜尋 (ANN)：使用快速方法找到相似的資料。  
哈希法 (Hashing)：用於快速識別大類別（topic）層級的相似性。  
樹狀搜尋 (Tree Search)：一種結構化的搜尋方式，提高搜尋效率。  

### 高維資料：

HNSW (Hierarchical Navigable Small Worlds)：通過多層次網絡結構，先大範圍搜尋，然後逐步縮小範圍，找到最近鄰。  
Scalable Approximate Nearest Neighbor (SANN)：可擴展的近似最近鄰搜尋方法，適用於大規模高維數據。  

### 資料庫支援

LODB 和 Cloud SQL PostgreSQL：為向量和嵌入搜尋提供支援。  

### 動態嵌入 (Evolving Embeddings)

非穩態嵌入：隨著資料更新，嵌入的向量表示需要重新訓練和調整，以保持準確性。  
