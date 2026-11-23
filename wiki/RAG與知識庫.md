# RAG 與知識庫

檢索增強生成（Retrieval-Augmented Generation, RAG）結合外部資料檢索與模型生成：系統先從知識庫找出相關內容，再提供給模型回答。Lewis 等人於 2020 年提出 RAG 架構，結合模型參數知識與可檢索外部記憶。[S06]

## 一般流程
1. 蒐集規則書、FAQ、官方文件與世界觀資料。
2. 前處理並保留標題、頁碼與版本。
3. 將文件切分成適當段落（Chunking）。
4. 建立索引或向量表示。
5. 依問題檢索相關段落。
6. 模型根據檢索內容生成答案並附來源。

OpenAI File Search 文件介紹 Responses API 的知識庫檢索；使用前需建立 vector store 並上傳檔案。[S04]

## 對 AI TRPG 的價值
查詢技能與戰鬥規則、讓 NPC 依世界觀設定對話、找回前次冒險紀錄，以及避免不同系統規則混用。

## 限制
檢索可能找錯段落；文件可能過時或矛盾；模型可能誤讀來源。附上連結不代表內容真的受到來源支持。

## 來源
- [S03] https://developers.openai.com/tracks/building-agents
- [S04] https://developers.openai.com/api/docs/guides/tools-file-search
- [S06] https://arxiv.org/abs/2005.11401