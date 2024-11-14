## LLM 如何產生這麼大的能力 

 主要透過 transformer - self attention 的機制
 
## LLM 模型們有何不同?  

GPT - decoder only model - Storyteller   
專注於預測下一個字，目的為完成故事  

BERT - encoder only model - Puzzle Master   
目標是補上缺失的文字，或者猜測下一個句子  

## LLM 的演變史

### GPT系列

GPT1 - unsupervised pre-training - 從未標註的大量資料中學習  
GPT2 - 10倍GPT1的訓練資料 10倍參數  
GPT3 - 175億參數 + few-shot learning (少樣本技術)  
GPT3.5, GPT4 - 可處理圖像 + 更多的文字區域 、 更長的回覆  

### Google 系列

LaMDA - 對話用語言模型 - 注重在對話更有人類感  
Gopher - 提升訓練效果與最佳化  
Chinchilla - data scaling 對於訓練有幫助  
PaLM - pathways language model  540B 參數  
PalM2 - smarter - code generation, math problems  
Gemini -  綜合google 前數代產品特性  
Gemini2 - 增長context window  
Gemini nano - 為了可攜式設備設計(便攜性)  
 
## 開源
meta、mistral ...

## Fine-tuning 為任務進行微調

Supervised Fine-Tuning (SFT) - 監督式微調：專注於特定專業領域，使用專業領域的data set  
Reinforcement Learning from Human Feedback (RLHF) - 使用人工訓練的評價系統(reward model)調整模型  
Parameter Efficient Fine-Tuning (PEFT) - 參數高效微調 以現實問題進行部分模型retrain參數  
