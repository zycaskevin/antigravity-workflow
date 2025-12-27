# GEMINI.md - Antigravity IDE 專案配置

> 此檔案為 Google Antigravity IDE 的專案級系統指令

## 🌐 語言設定

- **預設語言**: 繁體中文
- **腳本位置**: 所有 Hook 腳本必須存放於專案根目錄下的 .agent/hooks/ 資料夾。
- **配置檔案**: Hooks 的註冊、啟用與參數調整統一由 .agent/settings.json 管理。e
- **技術名詞**: 保留英文（API, Hook, Workflow, Component）
- **程式碼註解**: 中文
- **變數命名**: 英文 camelCase

---

## 📁 專案結構

```
專案根目錄/
├── .agent/                      # 🆕 Antigravity 配置
│   ├── rules/                   # 被動規則（始終生效）
│   │   ├── coding-standards.md  # 程式碼規範
│   │   ├── security-rules.md    # 安全規範
│   │   └── project-context.md   # 專案上下文
│   └── workflows/               # 主動工作流（/觸發）
│       ├── skill-eval.md        # /skill-eval
│       ├── code-review.md       # /code-review
│       ├── cleanup.md           # /cleanup
│       ├── debug.md             # /debug
│       ├── commit.md            # /commit
│       └── test.md              # /test
├── .claude/                     # Claude Code 配置
│   └── skills/                  # 模組化技能 (24個)
├── docs/                        # 文檔目錄
└── GEMINI.md                    # Antigravity 主配置（本檔案）
```

---

## ⚡ 快捷工作流

在對話中輸入 `/` 觸發以下工作流：

| 指令 | 用途 | 對應 Claude Skill |
|------|------|------------------|
| `/skill-eval` | 評估並激活相關技能 | UserPromptSubmit Hook |
| `/code-review` | 程式碼審查 | requesting-code-review |
| `/cleanup` | 清理臨時檔案並歸檔 | Stop Hook |
| `/debug` | 四階段系統性除錯 | systematic-debugging |
| `/commit` | 生成規範 Git commit | git-workflow |
| `/test` | 執行測試套件 | testing |

---

## 🛡️ 安全規範摘要

### 🔴 絕對禁止

- `rm -rf /`, `drop database`, `curl | bash`
- 硬編碼 API Key、密碼

### 🟡 需確認

- `git push --force`
- 寫入 `.env` 或認證檔案

### ✅ 自動放行

- 讀取類操作（`ls`, `cat`, `git status`）
- 建置類操作（`npm run build`）

詳見: `.agent/rules/security-rules.md`

---

## 🔧 開發規範摘要

### 程式碼風格

- JavaScript/TypeScript: ESLint + Prettier
- Python: PEP 8
- 所有函數必須有文檔註解

### 架構模式

- 後端: Controller → Service → DAO → Mapper
- 前端: 組件化 + 狀態管理集中

詳見: `.agent/rules/coding-standards.md`

---

## 📚 可用技能列表（24 個）

### 後端開發

- `crud-development`, `rest-api-design`, `spring-boot-crud`, `database-ops`
- `frontend-design`, `web-artifacts-builder`
- `ios-development`, `android-development`, `react-native-development`, `flutter-development`
- `mcp-builder`, `letta-agent`
- `testing`, `systematic-debugging`, `verification-before-completion`
- `git-workflow`, `writing-plans`, `executing-plans`
- `requesting-code-review`, `code-review-standards`
- `dispatching-parallel-agents`, `subagent-driven-development`
- `brainstorming`, `skill-creator`

詳見: `.agent/skills/` 目錄

---

## 🔄 Antigravity Standard

| 功能 | Antigravity Standard |
|------|-------------|
| 系統指令 | `GEMINI.md` |
| 被動規則 | `.agent/rules/` |
| 主動觸發 | `/workflow` |
| 技能文檔 | `.agent/skills/*.md` |

---

## 📋 工作流程

### 開始任務

1. 輸入 `/skill-eval` 評估需要的技能
2. 參考對應技能文檔的規範

### 開發中

1. 遵循 `.agent/rules/` 中的規範
2. 定期執行 `/test` 確認品質

### 完成任務

1. 執行 `/code-review` 自我審查
2. 執行 `/commit` 生成規範提交
3. 執行 `/cleanup` 清理並歸檔

---

**版本**: 1.0.0
**最後更新**: 2025-12-27
**維護者**: Claude Code + Gemini
