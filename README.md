# 🛸 Antigravity Workflows (AGW)

> **Turn your IDE into a Self-Correcting, Truth-Seeking Agent Operating System.**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Antigravity](https://img.shields.io/badge/Agent-Antigravity-blueviolet)](https://antigravity.google)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

**Antigravity Workflows** is a standardized configuration designed for Google Antigravity, Cursor, and Windsurf, transforming a "passive code editor" into an "active intelligent development partner."

[**中文文檔 (Traditional Chinese)**](README_CN.md)

---

## 🌟 Core Philosophy

Most AI tools are passive: You ask, they answer.
**Antigravity Workflows (AGW)** defines an **Active Lifecycle**:

1. **Truth > Obedience**: When a user requests a flawed solution, the system prioritizes finding the **Root Cause** over blind execution.
2. **Artifact-First**: All complex tasks must produce a plan or document before writing code.
3. **Systematic Debugging**: strict adherence to a 4-stage debugging process, rejecting "Try & Error" methodology.

---

## ⚡ Key Features

### 1. System Rules

Empower your AI with the following capabilities via `GEMINI.md` and `.agent/rules/`:

* **Safety Intercept**: Blocks `rm -rf` or dangerous `git push` commands.
* **Context Awareness**: Automatically reads project architecture and coding standards.
* **Artifact Archiving**: Automatically organizes development artifacts into `docs/`.

### 2. Power Workflows

Trigger with a simple Slash Command (`/`):

| Command | Function | It's like... |
|---------|----------|--------------|
| **/debug** | 4-Stage Root Cause Analysis (Investigate -> Pattern -> Hypothesis -> Fix) | Hiring a Senior Principal Engineer to debug for you |
| **/cleanup** | Smart cleanup of temp files and documentation archiving | An automated project janitor |
| **/skill-eval**| Assess required skills for the task and activate them | "Matrix Download" of skill sets |
| **/commit** | Generate Conventional Commits messages | A strict Tech Lead reviewing your commits |
| **/save** | Memory backup and meta-reflection (Requires Obsidian) | An AI diary and long-term memory |

---

## 🚀 Quick Start

### Installation

1. **Clone this project**:

    ```bash
    git clone https://github.com/zycaskevin/antigravity-workflow.git .
    ```

2. **Configure IDE**:
    * **Antigravity / Gemini Code Assist**: Set `GEMINI.md` as System Prompt or Project Instructions.
    * **Cursor**: Copy `.cursorrules` (if available) or paste `GEMINI.md` content into Project Rules.

3. **Start Using**:
    Type `/skill-eval` in the chat to test the system response.

---

## 📂 Structure

```
.
├── .agent/              # Core Agent Configuration
│   ├── rules/           # Passive Rules (Coding Style, Security)
│   └── workflows/       # Active Workflows (Debug, Cleanup, etc.)
├── .antigravity/        # IDE Specific Configs
├── GEMINI.md            # System Entry Point (System Prompt)
└── README.md            # This file
```

---

## 🤝 Contributing

We welcome all forms of contribution! Please see `CONTRIBUTING.md` (Coming Soon).

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

Distributed under the [MIT License](LICENSE).

---

<p align="center">Made with ❤️ by Antigravity Community</p>
