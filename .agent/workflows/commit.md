---
description: Git Commit
---

# Git Commit 工作流

> 觸發指令: `/commit`
> 用途: 生成規範的 Git commit

---

## 📋 執行流程

### 步驟 1 - 檢查變更狀態

```bash
git status
git diff --staged
```

### 步驟 2 - 分析變更類型

根據變更內容判斷 commit 類型：

| 類型 | 說明 | 範例 |
|------|------|------|
| `feat` | 新功能 | feat: 新增用戶登入功能 |
| `fix` | Bug 修復 | fix: 修復分頁計算錯誤 |
| `docs` | 文檔更新 | docs: 更新 API 使用說明 |
| `style` | 程式碼格式 | style: 調整縮排格式 |
| `refactor` | 重構 | refactor: 優化查詢邏輯 |
| `test` | 測試相關 | test: 新增單元測試 |
| `chore` | 雜項 | chore: 更新依賴版本 |

### 步驟 3 - 生成 Commit 訊息

#### 格式規範

```
<type>(<scope>): <subject>

<body>

<footer>
```

#### 範例

```
feat(auth): 新增 Google OAuth 登入

- 整合 Google OAuth 2.0
- 新增 AuthService.googleLogin()
- 更新用戶模型支援第三方登入

Closes #123
```

### 步驟 4 - 執行 Commit

```bash
git add .
git commit -m "<生成的訊息>"
```

---

## ⚠️ 安全檢查

執行 commit 前確認：

- [ ] 不包含敏感資訊（API Key, 密碼）
- [ ] 不包含 `.env` 檔案
- [ ] 不包含大型二進位檔案
- [ ] 測試已通過

---

## 📊 輸出格式

```markdown
## 📝 Commit 完成

### 變更摘要
- 類型: [feat/fix/docs/...]
- 範圍: [affected scope]
- 檔案數: X 個檔案
- 行數: +XX / -XX

### Commit 訊息
\`\`\`
[生成的完整 commit 訊息]
\`\`\`

### Commit Hash
\`[short hash]\`

### 下一步
- [ ] 推送到遠端: `git push`
- [ ] 建立 PR
```
