# Setup Guide: Memory & Sessions (VS Code 1.109+)

本指南将指导你如何在 VS Code 1.109+ 版本中配置和使用 GitHub Copilot 的最新特性：**Agent Session Management** 和 **Copilot Memory**。

## 1. Copilot Memory (项目偏好记忆)

Copilot Memory 允许 Copilot 记住你的项目特定偏好、架构决策和代码风格，从而在后续对话中提供更精准的建议。

### 开启与配置
1.  打开 VS Code 设置 (`Ctrl+,` / `Cmd+,`)。
2.  搜索 `github.copilot.memory`。
3.  确保勾选 **Enable** 选项。

### 使用方法
-   在 Chat 面板中，你可以直接告诉 Copilot 你的偏好。例如：
    > "在这个项目中，不管是前端还是后端，请总是使用 TypeScript，并且使用 async/await 风格。"
-   Copilot 会将这些信息存储在 memories 文件夹中，并使用这些信息来提供更准确和建议。

## 2. Agent Session Management (跨会话上下文保持)

VS Code 1.109 引入了更强大的会话管理功能，允许你在不同的工作区或时间点恢复之前的对话上下文。

### 主要功能
-   **历史记录访问**: 在 Chat 面板顶部，点击 "History" 图标（通常是一个时钟或列表图标），可以查看过去 30 天的对话记录。
-   **会话恢复**: 点击任意历史会话，Copilot 将恢复当时的上下文（包括当时引用的文件），你可以继续之前的讨论。
-   **跨窗口同步**: 如果你登录了 GitHub 账号，你的会话历史将在不同设备的 VS Code 之间同步。

### 最佳实践
-   **命名会话**: 虽然系统会自动生成标题，但建议手动重命名重要的会话（右键点击会话 -> Rename），以便日后检索。例如："Refactor Auth Module" 或 "Debug Memory Leak"。
-   **清理**: 定期删除不再需要的临时会话，保持历史记录整洁。

---
> **注意**: 确保你的 VS Code 处于最新版本 (Check for Updates)，部分 UI 元素可能随版本微调。
