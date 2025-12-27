---
description: 清理與歸檔工作流
---

# 清理與歸檔工作流 (Cleanup)

> 觸發指令: `/cleanup`
> 用途: 清理臨時檔案、歸檔文檔、更新索引
> 替代 Claude Code 的 Stop Hook

---

## 📋 執行流程

### 步驟 1 - 清理臨時檔案

刪除以下類型的臨時檔案：

```bash
# 測試臨時檔
test-*.js
test-*.ts
*.test.tmp

# 系統臨時檔
*.tmp
*.temp
*.swp
*~
nul

# 建置產物（可選）
# dist/
# build/
# node_modules/.cache/
```

### 步驟 2 - 文檔歸檔

將非白名單的 `.md` 檔案從根目錄移動至 `docs/`：

#### 白名單（保留在根目錄）

- `README.md`
- `CLAUDE.md`
- `GEMINI.md`
- `CHANGELOG.md`
- `LICENSE`
- `CONTRIBUTING.md`

#### 自動移動

```bash
# 這些檔案應移至 docs/
HOOKS_GUIDE.md → docs/HOOKS_GUIDE.md
API_DESIGN.md → docs/API_DESIGN.md
ARCHITECTURE.md → docs/ARCHITECTURE.md
```

### 步驟 3 - 更新 README 索引

在 `README.md` 中更新文檔索引區塊：

```markdown
## 📚 文檔索引

| 文檔 | 說明 |
|------|------|
| [HOOKS_GUIDE](docs/HOOKS_GUIDE.md) | Hooks 開發指南 |
| [API_DESIGN](docs/API_DESIGN.md) | API 設計文檔 |
| ... | ... |
```

---

## 📊 輸出報告

執行完成後輸出：

```markdown
## 🧹 清理完成報告

### 已刪除的臨時檔案
- [列出已刪除的檔案]
- 共 X 個檔案，釋放 X KB

### 已歸檔的文檔
- [原位置] → [新位置]

### README 索引更新
- ✅ 已更新 / ❌ 無需更新

### 專案狀態
- 根目錄檔案數: X
- docs/ 檔案數: X
- 臨時檔案: 0 ✅
```

---

## ⚠️ 注意事項

1. **不刪除**: `.git/`, `node_modules/`, `vendor/` 等依賴目錄
2. **確認再刪**: 大於 1MB 的檔案需確認
3. **備份提醒**: 建議在執行前 `git stash` 或 commit 變更
