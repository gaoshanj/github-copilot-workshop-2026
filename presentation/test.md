# Role
你是一位严谨的 GitHub 官方技术布道师。你的任务是**彻底重构** `presentation/slides.md`，确保所有知识点（特别是 Copilot CLI）与**2025-2026 最新官方文档**完全一致，并解决之前的 Mermaid 渲染和页数不足问题。

# Critical Corrections (必须严格执行)

## 1. 彻底修正 GitHub Copilot CLI 内容
**严禁**使用旧的 `gh copilot suggest/explain` 命令描述。必须基于最新官方文档 (github.blog/ai-and-ml/github-copilot/github-copilot-cli-how-to-get-started/) 进行编写：
- **安装方式**: `npm install -g @github/copilot` (注意包名)。
- **启动方式**: 终端输入 `copilot`，然后 `/login`。
- **核心定位**: 它是**终端里的全能 Agent**，而不仅仅是命令建议工具。
- **关键能力演示** (必须包含以下场景):
  1. **项目理解**: "Explain the layout of this project." (自动扫描文件结构)
  2. **环境检查**: "Make sure my environment is ready to build." (自动安装缺失依赖)
  3. **Issue 挖掘**: "Find good first issues and rank them." (调用 GitHub MCP Server)
  4. **代码实现**: "Start implementing issue #1234. Show me the diff before applying." (自动改代码并展示 Diff)
  5. **Git 工作流**: "Stage changes, write a commit referencing #1234, and open a draft PR." (全自动 Git 操作)
  6. **系统运维**: "What process is using port 8080? Kill it." (自动查找并杀进程)
- **安全机制**: 强调 **"Ask Before Run"** 机制 (Allow once/Allow always/Deny)。
- **MCP 扩展**: 提及 `/mcp` 命令可扩展连接其他服务。

## 2. 修复 Mermaid 图表渲染
- **语法强制**: 所有流程图、架构图必须使用标准的 ````mermaid` 代码块。
- **Frontmatter 配置**: 必须在文件头部明确声明 `mermaid: true`。
- **图表数量**: 全文至少包含 **6 个** 高质量 Mermaid 图表：
  1. CLI 工作流程图 (用户输入 -> AI 计划 -> 用户授权 -> 执行命令)。
  2. MCP 架构示意图 (Copilot CLI <-> GitHub MCP Server <-> GitHub API)。
  3. Agent Session 状态流转图。
  4. Inline vs Panel 模式对比图。
  5. Custom Instructions 作用域示意图。
  6. Skills 加载与执行流程图。

## 3. 扩充内容至 45-50 页 (严格配额)
请按以下结构逐页生成，不得合并页面：
- **封面与引言 (4页)**: 标题、讲师、议程、环境检查清单 (Node v22+, npm v10+, VS Code 1.109+)。
- **模块一：基础交互 (12页)**: 
  - Session 管理图解。
  - Memory 配置步骤。
  - Inline vs Panel 对比 (分栏布局 + 案例)。
  - 3 个实操案例 (每案 2 页)。
- **模块二：进阶定制 (14页)**: 
  - Custom Instructions 详解 (4 页)。
  - Agent vs Plan 模式行为差异 (Mermaid 时序图)。
  - MCP 协议架构与配置 (4 页)。
  - 故障排除 (2 页)。
- **模块三：CLI 与 Skills (14页)**: 
  - **CLI 安装与启动** (2 页，含 npm 命令)。
  - **CLI 核心场景实战** (6 页，上述 6 个场景各 1 页，含真实对话截图模拟)。
  - **CLI 安全机制** (2 页，详解 Allow/Deny 流程)。
  - **Skills 开发规范** (4 页，Manifest 结构 + 示例)。
- **总结与实验 (4页)**: 知识地图、实验任务卡、Q&A。

## 4. 视觉与版式规范 (GitHub Dark Theme)
- **Frontmatter 配置** (必须包含):
  ```yaml
  ---
  marp: true
  theme: gaia
  class: lead
  backgroundColor: #0d1117
  color: #c9d1d9
  style: |
    section { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif; }
    h1, h2, h3 { color: #58a6ff; }
    code { background: #161b22; color: #e6edf3; padding: 0.2em 0.4em; border-radius: 6px; }
    pre { background: #161b22; border: 1px solid #30363d; }
    .columns { display: grid; grid-template-columns: 1fr 1fr; gap: 2rem; }
  mermaid: true
  ---
- 演讲者备注: 每页底部必须包含 <!-- speaker_note: ... -->，内容需包含：
 - 操作指引: "现在请大家打开终端，输入 copilot..."
 - 互动问题: "大家猜猜 Copilot 会先执行哪条命令？"
 - 避坑指南: "注意：如果没安装 Node v22+，这里会报错..."

# Action Plan
## 第一步: 创建新的 slides_modify.md，写入正确的 Frontmatter 和 CSS。
## 第二步: 按照上述页数配额，逐页编写内容。
- CLI 部分: 严格使用 copilot 命令和自然语言交互案例，禁止编造子命令。
- 图表部分: 插入 6+ 个 Mermaid 代码块。
- 引用部分: 代码示例直接从 Repo 中引用。
## 第三步: 在文件末尾添加 "环境准备指南"，明确列出：
- 安装 Node.js v22+
- 安装 @github/copilot: npm install -g @github/copilot
- 安装 VS Code 插件: Marp for VS Code (用于预览 Mermaid)
## 第四步: 自我验证：
- 总页数 >= 45？
- CLI 命令是否全部为 copilot 且符合官方博客描述？
- 是否包含 6 个 Mermaid 图表？
- 每页是否有演讲者备注？