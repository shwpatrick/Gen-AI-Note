# 第四章 ：Solving Domain-Specific Problems Using LLMs

fine-tune LLM 以處理特殊領域的問題  

Sec LM - Cyber Security  
Med LM - Healthcare  

## Sec LM - Cyber Security

### 資安三個問題
   
- 威脅 - 攻擊越來越複雜  
- 辛苦 - 維運開發費時費力  
- 人才 - 人才缺乏  

### Gen AI 在任務中的劃分階層

- 頂層：理解現有資料和安全工具  
- 中層：推理能力與API  
- 底層：有效安全情報和運營知識  

### Sec LM 關注重點：

- 新鮮度：威脅與漏洞的更新  
- 使用者特定資料：安全資料不會暴露  
- 安全專業知識：理解安全知識與術語  
- 使用者特定數據：可以組合多個資料來源與模型  

### 通用語言模型的問題

- 缺乏公開安全數據訓練  
- 訓練資訊缺乏深度  
- 敏感內容禁用  

### Sec LM 建構順序
 
1.強力的基礎模型  
2.pre-training -> security spec  
3.fine-tuning  
4.RAG  

## Med PalM - Healthcare

### 醫療的Gen AI應用場景：

- 根據用戶健康史回覆  
- 綜合分析病患語意  
- 參考患者反映調整回饋  
- 提供即時資訊作為醫師助手  

### 引入整合細化(ER)

1. 透過溫度隨機採樣多種解釋與答案  
2. 透過第一階段的答案群進行解釋(答案聚合)  

## 對於kaggler 的用途  

分析藥學資料關聯性 重要性 等等  
