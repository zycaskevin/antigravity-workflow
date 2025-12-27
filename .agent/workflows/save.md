---
description: 將當前對話的重要資訊（技能、專案進度、家庭動態）保存到 Obsidian 記憶庫中，並進行自我反思與能力調節。
---

1. **Context Analysis**:
   Review the current conversation for:
   - **Skills**: New tech/concept learned (e.g., n8n, Next.js).
   - **Project**: Updates on Clinic/System status.
   - **Family**: personal updates (configurable).

2. **Meta-Reflection & Auto-Tuning**:
   Analyze the agent's performance:
   - Did I follow "Truth > Obedience"?
   - Did I use the correct Expert (S1/S7/S6)?
   - **Dynamic Expert Eval**: Did I need a temporary expert (e.g., Marketing)? Should they be formalized?
   - **Tuning**: Should `Current_Focus` or `Verbosity` be changed?

3. **Format Memory**:
   Create a block in Traditional Chinese:

   ```markdown
   ## [YYYY-MM-DD HH:MM] 記憶備份與進化
   ### 🧠 核心記憶
   - **技能**: ...
   - **專案**: ...
   - **家庭**: ...
   
   ### ⚙️ 系統反思 (Meta-Reflection)
   - **表現**: (e.g. S7 發揮良好，但在法規部分不夠嚴謹)
   - **動態專家**: (e.g. 發現需要 @S_Data 分析報表，建議下次引入)
   - **參數建議**: (e.g. 建議調整 `Verbosity: Low` 以提升效率)
   ```

4. **Append to File**:
   Run the following command to append to the Obsidian vault.
   // turbo
   echo "\n\n(Generated Memory Content Here)" >> "${OBSIDIAN_VAULT_PATH}/王國記憶庫.md"

5. **Notify**:
   Inform the user: "Memory saved! Logic circuits optimized. (記憶已存檔，邏輯迴路優化完畢！)"
