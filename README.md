# Terminal 操作入門

**Project Kickoff Skill · iLink Professional認證實作專案**

中央研究院社會學研究所 / 輔仁大學 社會學系  
林文正 博士後研究員

以一次一題的引導訪談，協助新手建立有秩序、可維護、可接續的專案。先建立好的管理架構，資料品質才有檢查依據，後續更新也有固定方法。

## 這個專案要解決什麼問題？

教育與研究工作者使用 AI 協助工作時，可能不知道如何開始、資料要放在哪裡，也不熟悉終端機與版本管理。若需求、品質規則及進度只留在聊天裡，換一輪對話仍可能重新找資料、重新解釋或重做修正。

| 問題 | 影響 | 本專案的做法 |
| --- | --- | --- |
| 不會寫完整需求與配置指令 | 開工困難、反覆補充需求 | 短指令啟動，一次問一題；不知道時提供建議 |
| 檔案散落，來源與版本不明 | 用錯資料、難以接手 | 依需求規劃資料夾，建立用途說明與來源索引 |
| 品質與修正缺少規則 | 錯值帶入成果、無法追溯 | 確認檢查條件，保留原檔，修正另存並保存證據 |
| 決策與進度未更新 | Context 混入過期資訊，AI 重問、重讀與重做 | 規則及進度寫入檔案，持續更新索引，接續先核對狀態 |

這些重複工作可能增加時間與無效 Token 使用。本專案以改善開工、資料管理與交接流程為目標，尚未量測實際 Token 節約率。

## 如何開始？

1. 下載本儲存庫 ZIP，取出完整 `skill/project-kickoff/` 資料夾。
2. 放入個人 `~/.claude/skills/project-kickoff/`，或專案 `.claude/skills/project-kickoff/`。已有同名版本時先比較，不只複製 SKILL.md。
3. 在選定工作目錄啟動 Claude Code，輸入：

```text
/project-kickoff
```

用自己的話回答，例如「我要整理這學期的課程資料」。助手先讀現況，再逐題補問。需要建議時說「請幫我建議」，不必先貼長串 prompt。

[完整 Skill 使用與安裝指南](skill/project-kickoff/README.md) · [Skill 主指引](skill/project-kickoff/SKILL.md)

## 設計與產出

```text
讀取現況 → 逐題補問 → 提出配置方案 → 依授權建檔 → 核對結果 → 保存與接續
```

依用途選擇必要資料夾，產生專案 README、CLAUDE、PROGRESS、各庫用途說明，以及適用的 DATA_RULES 與 .gitignore。整理需求可選盤點建索引、整理副本、檢查清理或歸檔；選擇方式不代表任意搬檔、覆寫或刪除授權。

Skill 將訪談、配置與交接轉成可重用的 AI Agent 工作指引，讓使用者從需求與判斷開始，降低自行拼湊設定的負擔。建立配置不等於資料品質已通過檢查，仍須實際驗證與維護。

[資料管理規則](skill/project-kickoff/references/data-management.md) · [Context 管理規則](skill/project-kickoff/references/context-strategy.md)

## 互動教材

- [index.html](index.html)：Terminal 操作入門，十頁互動教材。
- [project-report-interactive.html](project-report-interactive.html)：互動專案報告。
- [project-kickoff.skill](project-kickoff.skill)：ZIP 格式 Skill 封裝，可解壓安裝。

下載 HTML 後以瀏覽器開啟，無須伺服器。教材包含逐步問答與資料夾產出動畫、資料管理說明、配置建置器及五題測驗。網頁終端機與時間／Token 比較為教學模擬，不會執行 AI 或修改電腦檔案。

## 驗證與使用邊界

既有模擬案例及單一交接檔恢復案例各通過 8 項檢查；沒有直接驗證系統內部自動壓縮。最新逐題訪談與整理選項、真人學習成效及 Token 節約仍待實測。

保留來源原檔，不自行公開受限資料或推送。保存不等於壓縮，Skill 不修改模型容量或系統門檻。建立資料庫位置、歸檔位置或備份庫，不代表已匯入資料、完成歸檔或驗證還原。

## 參考資料

- [Claude Code Skills](https://code.claude.com/docs/en/skills)
- [Context window](https://code.claude.com/docs/en/context-window)
- [Manage costs effectively](https://code.claude.com/docs/en/costs)
