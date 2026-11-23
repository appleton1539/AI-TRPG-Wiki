# AI 與大型語言模型

## LLM 是什麼？
大型語言模型（Large Language Model, LLM）能依上下文生成文字，可用於摘要、改寫、角色對話與規劃，但生成流暢不代表內容必然正確。

## Prompt
Prompt 是提供給模型的指令與上下文。跑團 Prompt 應說明 AI 的角色、任務、限制與輸出格式，例如：不可替玩家決定重大行動；不可擅自改寫角色數值；遇到規則缺漏先詢問。

Prompt 能引導行為，但不能單獨保證長期記憶、規則正確或狀態一致。

## Agent
AI Agent 把模型、指令、工具與執行流程組合起來。它可能透過工具查資料、讀取角色表、擲骰或更新資料。[S03]

## Function Calling
工具呼叫讓模型提出結構化功能請求，例如要求擲骰。應用程式接收請求、驗證參數、實際執行，再把結果交回模型。模型提出呼叫不等於動作已執行。[S05]

## 來源
- [S03] https://developers.openai.com/tracks/building-agents
- [S05] https://developers.openai.com/api/docs/guides/function-calling