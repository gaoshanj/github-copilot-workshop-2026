# Inline Chat vs Panel Chat: 场景对比实战

GitHub Copilot 提供了两种主要的交互模式：**Inline Chat (行内对话)** 和 **Panel Chat (侧边栏对话)**。理解它们的区别对于提升效率至关重要。

## 1. 核心区别

| 特性 | Inline Chat (`Ctrl+I` / `Cmd+I`) | Panel Chat (`Ctrl+Alt+I` / `Cmd+L`) |
| :--- | :--- | :--- |
| **主要用途** | 快速修改、生成代码、修复错误 | 复杂问答、架构设计、多文件理解、解释代码 |
| **上下文** | 聚焦于当前文件或选中的代码块 | 拥有整个工作区（Workspace）的更广阔视野 |
| **交互方式** | 直接在编辑器中以 Diff 形式展示修改 | 在侧边栏对话，需要手动 Apply 或 Insert 代码 |
| **适用场景** | "把这个函数改成异步"、"修复这里的 bug" | "如何设计这个模块？"、"解释这段代码的逻辑" |

## 2. 实战案例

### 场景 A: 快速修复 (使用 Inline Chat)

**任务**: 将一个普通的求和函数转换为支持可变参数的箭头函数。

1.  打开 `01-basics/examples/calculator.js`。
2.  选中 `add` 函数。
3.  按下 `Ctrl+I` (Windows) / `Cmd+I` (Mac)。
4.  输入提示词: *"Convert to arrow function and support variable arguments"*
5.  **观察**: Copilot 直接在代码原地展示 Diff，按下 `Accept` (Ctrl+Enter) 即可应用。

### 场景 B: 复杂重构与解释 (使用 Panel Chat)

**任务**: 理解并重构一个遗留类，增加错误处理。

1.  打开 `01-basics/examples/legacy-processor.js` (如有)。
2.  打开侧边栏 Chat 面板。
3.  输入提示词: *"@workspace Explain what this file does and suggest how to add error handling for network requests."*
4.  **观察**: Copilot 会分析代码逻辑，并在侧边栏给出详细的解释和建议代码块。你需要点击代码块上方的 "Insert at Cursor" 按钮来应用更改。

## 3. 混合使用技巧

*   先用 **Panel Chat** 制定计划或理解逻辑。
*   再用 **Inline Chat** 执行具体的代码落地。
*   **Agent Mode**: 在 Panel Chat 中使用 `@agent` (如果可用) 可以让 AI 自主执行多步操作，类似于 Inline Chat 的自动执行能力，但拥有 Panel 的上下文深度。
