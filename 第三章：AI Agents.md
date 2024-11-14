## AI Agent 與 Model 的差別為何?

Agent 非一個只等待輸入的model，它能夠自己理解並確定下一步驟以達到目標  

- model 靜態 - 的受限於訓練資料  
- agent 動態 - 具備能力拓展 - 工具以及目標  

## AI Agent 的組成?

Agent 由三個部分組成：  

- Model - 負責進行決策(大腦)  
- Tool - 負責大腦與外界的聯繫(手)  
- Orchestration - 負責將維護記憶、 狀態、推理和規劃  

## Model 

在這裡指的是語言模型框架，可以進行決策溝通與推理，常用的模型如下：

- ReAct：⼀個即時⼯程框架，為語⾔模型提供思考過程策略  
- Chain-of-Thought(CoT)：⼀種⽀持推理的快速⼯程框架  
- Tree-of-Thought(ToT)：⼀個快速的⼯程框架，適合 探索或策略前瞻性任務。作為使⽤語⾔模型解決⼀般問題的中間 步驟  

## Tool

語言模型的觸手，使得它可以與外界交互，工具可以分成以下三類：

- Extension 
- Functions 
- Data stores. 
### Extension (API專家)

負責與外界API交互，將內容轉換成API可以使用的語法格式，功能也包括將API回應轉換為系統可用的語法，甚至可以在此放入open api specifications，讓系統透過Spec 理解如何使用 API 或者選擇適合場景的API

但有些API會遇到下列問題：

- API 呼叫需要在應⽤程式堆疊的另⼀層
- 阻⽌代理直接呼叫API 的安全或⾝份驗證限制（例如API 不暴露於互聯網，或代理基礎設施無法存取 )
- 阻⽌代理程式進⾏ API 呼叫的時間或操作順序約束 即時的。 （即批量操作、⼈機互動審核等）  

等等。這些時候就會透過Functions來控制API
### Functions 

控制Agent的程式碼，使得有些內容可以透過程式碼客製實現，不用全部都透過API處理。有時候也在此控制API。
### data stores - 使agent可以儲存多於初始化的知識

例如AI助手協助解題，從wiki或者更多外部資料得到幫助

## 如何確保 agent 用tool 的效率

targeted learning - fine-tune agent

三種方法 - 這幾個方法可以混用

- in-context learning - prompt 時給予工具 範例 - 不用額外training
- context learning - retrieval based - 給整個資料庫當參考
- fine-tuning based learning - 拿特殊的dataset予以訓練作為微調
 
## 如何實作Agent AI

Lang Chain - 一種高階程式語言專門用來設計Agent
當已有data, model 等等具備條件，可以使用lang chain 進行編排

API 範例 serp API
