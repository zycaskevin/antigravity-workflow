---
description: 測試執行工作流
---

# 測試執行工作流

> 觸發指令: `/test`
> 用途: 執行測試套件並分析結果

---

## 📋 執行流程

### 步驟 1 - 偵測測試框架

自動偵測專案使用的測試框架：

| 檔案/目錄 | 框架 | 執行命令 |
|----------|------|---------|
| `vitest.config.*` | Vitest | `npm run test` |
| `jest.config.*` | Jest | `npm test` |
| `playwright.config.*` | Playwright | `npx playwright test` |
| `pytest.ini` | Pytest | `pytest` |
| `pom.xml` (with JUnit) | JUnit | `mvn test` |

### 步驟 2 - 執行測試

```bash
# 根據偵測結果執行對應命令
npm run test
# 或
pytest
# 或
mvn test
```

### 步驟 3 - 分析結果

#### 成功 ✅

```markdown
## ✅ 測試通過

- 總測試數: XX
- 通過: XX
- 略過: XX
- 執行時間: X.XXs
- 覆蓋率: XX%
```

#### 失敗 ❌

```markdown
## ❌ 測試失敗

### 失敗的測試
| 測試名稱 | 檔案 | 錯誤類型 |
|---------|------|---------|
| [test name] | [file:line] | [error type] |

### 錯誤詳情
\`\`\`
[完整錯誤訊息]
\`\`\`

### 建議修復方向
1. [根據錯誤訊息的分析建議]
```

---

## 🎯 測試策略建議

### 單元測試 (Unit)

- 覆蓋率目標: 80%+
- 測試獨立函數和方法
- Mock 外部依賴

### 整合測試 (Integration)

- 測試模組間互動
- 使用測試資料庫
- 驗證 API 端點

### E2E 測試 (End-to-End)

- 測試關鍵用戶流程
- 使用 Playwright/Cypress
- 涵蓋主要使用場景

---

## 📊 輸出格式

```markdown
## 🧪 測試報告

### 執行摘要
| 指標 | 數值 |
|------|------|
| 總測試數 | XX |
| 通過 | XX ✅ |
| 失敗 | XX ❌ |
| 略過 | XX ⏭️ |
| 覆蓋率 | XX% |
| 執行時間 | X.XXs |

### 覆蓋率細節
| 類型 | 覆蓋率 |
|------|--------|
| 行覆蓋 | XX% |
| 分支覆蓋 | XX% |
| 函數覆蓋 | XX% |

### 下一步行動
- [根據結果的建議]
```
