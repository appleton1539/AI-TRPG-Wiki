# AI 跑團流程

## 一次互動
1. 玩家輸入角色行動。
2. 系統載入場景、角色卡與相關規則。
3. LLM 判斷是否需要查詢規則或呼叫工具。
4. 若需擲骰，由程式工具產生結果。
5. 規則引擎驗證結果與狀態變更。
6. LLM 根據已驗證結果敘述後果。
7. 儲存新狀態與本回合摘要。

## 範例：翻越古牆
玩家想翻過石牆避開巡邏兵。RAG 查詢攀爬／潛行規則；LLM 判斷是否需要檢定並說明風險；工具執行骰子；規則引擎檢查結果與資源；LLM 再敘述後果。

## 例外處理
- 找不到規則：詢問 GM 或標示臨時裁定。
- 檢索到多套規則：先確認正在使用哪套系統。
- 工具執行失敗：保留原狀態，不可先宣稱成功。
- 玩家行動不清楚：提出必要澄清。
- 生成內容與狀態衝突：退回修正。

## 可觀測性
記錄玩家輸入、檢索來源、工具參數、骰子結果、狀態差異與模型輸出，方便追查錯誤與 GM 覆核。

## 來源
- [S03] https://developers.openai.com/tracks/building-agents
- [S05] https://developers.openai.com/api/docs/guides/function-calling
- [S08] https://www.cis.upenn.edu/~ccb/publications/labyrinth-ai-gm.pdf