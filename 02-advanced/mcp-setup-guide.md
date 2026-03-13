# MCP (Model Context Protocol) Setup Guide

This guide explains how to configure MCP servers to connect GitHub Copilot with local resources like SQLite databases and the filesystem.

## Prerequisites
-   VS Code 1.109+
-   GitHub Copilot Chat Extension (Latest)
-   Node.js v18+ (for running MCP servers)
-   `uv` (for Python-based servers) or `npm` (for Node.js-based servers)

## 1. Understanding MCP
MCP allows Copilot to "talk" to external tools. You define these tools in a configuration file, and Copilot can then query them (e.g., "Query the users table in my database").

## 2. Configuration File
VS Code looks for MCP configuration in specific locations. You can also configure it directly in VS Code settings.

**Location**:
-   Windows: `%APPDATA%\Code\User\globalStorage\ms-vscode.copilot-chat\mcp-servers.json` (typical path, may vary)
-   Mac/Linux: `~/.config/Code/User/globalStorage/ms-vscode.copilot-chat/mcp-servers.json`

## 3. Setting up SQLite MCP

1.  Ensure you have `uv` installed (or use `pipx`).
2.  Use the configuration provided in `mcp-configs/sqlite-mcp.json`.
3.  Add the JSON content to your global MCP settings file.
4.  **Restart VS Code**.
5.  **Test**: Open Chat and ask: *"List all tables in the connected database."* (Make sure `test.db` exists or point to a valid DB).

## 4. Setting up Filesystem MCP

1.  Use the configuration provided in `mcp-configs/filesystem-mcp.json`.
2.  Adjust the path `./allowed-directory` to an absolute path you want Copilot to access.
3.  Add to global MCP settings.
4.  **Restart VS Code**.
5.  **Test**: Ask Copilot: *"Read the file 'notes.txt' from the allowed directory."*

## Troubleshooting
-   **Connection Refused**: Ensure the command (npx/uvx) works in your terminal.
-   **Not Found**: Verify the paths in the JSON config are absolute or correctly relative to where VS Code launches the server.
