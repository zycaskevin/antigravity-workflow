---
description: 技能評估工作流 (Skill Evaluation)
---

# 技能評估工作流 (Skill Evaluation)

> 觸發指令: `/skill-eval`
> 用途: 評估用戶請求並激活相關技能

---

## 📋 執行流程

### 步驟 1 - 分析用戶請求

提取用戶請求中的關鍵字，識別任務類型。

### 步驟 2 - 評估技能相關性

針對以下每個技能，輸出：【技能名】- 是/否 - 【理由】

## 🛠️ 可用技能列表

### 後端開發

| 技能 | 觸發關鍵字 |
|------|-----------|
| crud-development | CRUD、增刪改查、業務模塊、Entity、Service、DAO |
| rest-api-design | REST、API、HTTP、端點、分頁、錯誤處理 |
| spring-boot-crud | Spring Boot、JPA、DDD、Aggregate |
| database-ops | 資料庫、PostgreSQL、SQL、索引、RLS |

### 前端開發

| 技能 | 觸發關鍵字 |
|------|-----------|
| frontend-design | 前端、UI、UX、設計、美學 |
| web-artifacts-builder | HTML、React、shadcn、單頁應用 |

### 移動端開發

| 技能 | 觸發關鍵字 |
|------|-----------|
| ios-development | iOS、iPhone、Swift、SwiftUI |
| android-development | Android、Kotlin、Compose |
| react-native-development | React Native、Expo |
| flutter-development | Flutter、Dart、BLoC |

### 整合與工具

| 技能 | 觸發關鍵字 |
|------|-----------|
| mcp-builder | MCP、Model Context Protocol |
| letta-agent | Letta、Agent、持久記憶 |

### 品質保證

| 技能 | 觸發關鍵字 |
|------|-----------|
| testing | 測試、TDD、BDD、單元測試、E2E |
| systematic-debugging | 除錯、Bug、錯誤、根因分析 |
| verification-before-completion | 驗證、完成、確認 |

### 協作流程

| 技能 | 觸發關鍵字 |
|------|-----------|
| git-workflow | Git、分支、commit、PR |
| writing-plans | 計畫、任務分解、規劃 |
| executing-plans | 執行、批次、檢查點 |
| requesting-code-review | Code Review、審查、PR |
| receiving-code-review | Review 回應、反饋處理 |

### 進階協作

| 技能 | 觸發關鍵字 |
|------|-----------|
| dispatching-parallel-agents | 並行、多任務、Agent |
| subagent-driven-development | Subagent、兩階段 Review |
| brainstorming | 腦力激盪、創意、探索 |
| skill-creator | 創建技能、新增 Skill |

---

## 步驟 3 - 輸出格式

```markdown
## 🎯 技能評估結果

| 技能 | 相關性 | 理由 |
|------|--------|------|
| [技能名] | ✅ 是 / ❌ 否 | [簡要說明] |

### 建議激活的技能
1. **[技能名]** - [用途說明]

### 下一步行動
[根據評估結果建議的具體行動]
```

---

## 步驟 4 - 載入技能指南

如果評估結果為「是」，自動參考對應的技能文檔：

- 位置: `.agent/skills/[skill-name].md`
- 遵循技能文檔中的開發規範和禁止事項
