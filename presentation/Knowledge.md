# GitHub Copilot Workshop 2026 - Knowledge Base

## 1. VS Code Updates (v1.109 & v1.110 - Early 2026)
### v1.110 (Feb 2026)
*   **Agent Plugins**: Bundle slash commands, skills, agents, and MCP servers into installable extensions.
*   **Agentic Browser Tools**: Native browser control (open, click, screenshot, console logs) for agents.
*   **Session & Plan Memory**: Persist plans and context across sessions/CLI/reviews.
*   **Context Management**: `/compact` command to manually condense context.
*   **Fork Session**: Branch conversations to explore alternative solutions.
*   **Lifecycle Hooks**: Run shell commands at agent events (pre/post-execution).

### v1.109 (Jan 2026)
*   **Multi-Agent Orchestration**: Parallel sub-agents for complex tasks.
*   **Copilot Memory (Preview)**: Cross-session context retention.
*   **Mermaid Support**: Interactive diagrams in chat responses.
*   **Terminal Sandboxing**: Safer command execution (macOS/Linux).
*   **Claude Integration**: Native support for Claude models in Copilot.

## 2. Copilot CLI (The New Standard)
*   **Package**: `@github/copilot` (npm)
*   **Install**: `npm install -g @github/copilot`
*   **Auth**: Run `copilot` -> `/login` (Device Flow)
*   **Key Concept**: "Terminal Agent" (not just a wrapper)
*   **Command**: `copilot` (interactive session)
*   **Safety**: "Ask Before Run" (Allow once, Allow always, Deny)

### Core Scenarios (Must Demo)
1.  **Project Understanding**: `Explain the layout of this project.` -> Scans file tree.
2.  **Environment Check**: `Make sure my environment is ready to build.` -> Checks node/npm versions.
3.  **Issue Triage**: `Find good first issues and rank them.` -> Connects to GitHub API via MCP.
4.  **Implementation**: `Start implementing issue #1234.` -> Generates code, shows diff.
5.  **Git Workflow**: `Stage changes, write a commit referencing #1234, and open a draft PR.`
6.  **Ops/System**: `What process is using port 8080? Kill it.`

## 3. Advanced Features
*   **Agent Mode**: Autonomous execution (multi-step, tool use).
*   **Plan Mode**: Chain-of-thought planning (step-by-step breakdown).
*   **MCP**: Standard protocol for connecting AI to local/remote data (SQLite, Filesystem).
*   **Custom Instructions**: `.github/copilot-instructions.md`.
*   **Prompt Files**: `.prompt.md` for reusable tasks.

## 4. Visuals (Mermaid)
*   **CLI Workflow**: Input -> Plan -> Authorization -> Execution.
*   **MCP Architecture**: VS Code -> MCP Server -> Data.
*   **Session Flow**: State diagram of a chat session.
*   **Inline vs Panel**: Decision tree for when to use which.
*   **Skills Lifecycle**: How a skill is loaded and executed.
*   **Agent vs Plan**: Sequence diagram comparing modes.

## 5. Environment Requirements
*   Node.js v22+
*   npm v10+
*   VS Code 1.109+
