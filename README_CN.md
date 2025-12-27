# 🛸 Antigravity Workflows (AGW)

> **Turn your IDE into a Self-Correcting, Truth-Seeking Agent Operating System.**
> 讓你的 IDE 成為具備自我修正、追求真理能力的 AI 代理作業系統。

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Antigravity](https://img.shields.io/badge/Agent-Antigravity-blueviolet)](https://antigravity.google)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

**Antigravity Workflows** 是一套專為 Google Antigravity、Cursor 與 Windsurf 設計的標準化配置，旨在將「被動的程式碼編輯器」轉化為「主動的智能開發夥伴」。

---

## 🌟 核心理念 (Core Philosophy)

大多數 AI 輔助工具是被動的：你問，它答。
**Antigravity Workflows (AGW)** 定義了一套 **主動生命週期 (Active Lifecycle)**：

1. **Truth > Obedience (真理 > 服從)**：當用戶要求錯誤的解決方案時，系統會優先尋求根因 (Root Cause)，而非盲目執行。
2. **Artifact-First (產物優先)**：所有複雜任務必須先產出計畫或文件，而非直接寫程式碼。
3. **Systematic Debugging (系統化除錯)**：拒絕 "Try & Error"，強制的四階段除錯流程。

---

## ⚡ 核心功能 (Key Features)

### 1. 系統級自律規則 (System Rules)

通過 `GEMINI.md` 與 `.agent/rules/`，賦予 AI 以下能力：

* **安全攔截**：阻止 `rm -rf` 或危險的 `git push`。
* **上下文感知**：自動讀取專案架構與編碼規範。
* **工具歸檔**：自動整理開發產物至 `docs/`。

### 2. 強大工作流 (Power Workflows)

只需輸入 Slash Command (`/`) 即可觸發：

| 指令 | 功能 | 就像是... |
|------|------|-----------|
| **/debug** | 四階段根因分析 (調查 -> 模式 -> 假設 -> 修復) | 請了一位資深首席工程師幫你 Debug |
| **/cleanup** | 智能清理臨時檔案並歸檔文檔 | 專案的自動掃地機器人 |
| **/skill-eval**| 評估當前任務需要的技能並激活 | 矩陣下載 (Matrix Download) 技能包 |
| **/commit** | 生成 Conventional Commits 規範的訊息 | 嚴格的 Tech Lead 審查 Commit |
| **/save** | 記憶備份與自我反思 (需設定 Obsidian) | AI 的日記與長期記憶 |

---

## 🚀 快速開始 (Quick Start)

### 安裝 (Installation)

1. **Clone 本專案**：

    ```bash
    git clone https://github.com/zycaskevin/antigravity-workflow.git .
    ```

2. **配置 IDE**：
    * **Antigravity / Gemini Code Assist**: 將 `GEMINI.md` 設定為 System Prompt 或 Project Instructions。
    * **Cursor**: 複製 `.cursorrules` (若有) 或將 `GEMINI.md` 內容貼入 Project Rules。

3. **開始使用**：
    在對話框中輸入 `/skill-eval` 測試系統反應。

---

## 📂 目錄結構 (Structure)

```
.
├── .agent/              # Agent 核心配置
│   ├── rules/           # 被動規則 (Coding Style, Security)
│   └── workflows/       # 主動工作流 (Debug, Cleanup, etc.)
├── .antigravity/        # IDE 特定配置
├── GEMINI.md            # 系統入口 (System Prompt)
└── README.md            # 本文件
```

---

## 🤝 貢獻 (Contributing)

我們歡迎所有形式的貢獻！請參閱 `CONTRIBUTING.md` (Coming Soon)。

1. Fork 本專案
2. 建立你的 Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit 你的變更 (`git commit -m 'Add some AmazingFeature'`)
4. Push 到 Branch (`git push origin feature/AmazingFeature`)
5. 開啟 Pull Request

---

## 📄 授權 (License)

本專案採用 [MIT License](LICENSE)。

---

<p align="center">Made with ❤️ by Antigravity Community</p>
