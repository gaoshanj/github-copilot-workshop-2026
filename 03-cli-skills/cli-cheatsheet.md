# GitHub Copilot CLI Cheatsheet

## Basic Usage
| Command | Description | Example |
| :--- | :--- | :--- |
| `gh copilot suggest "<query>"` | Suggest a shell command for a task | `gh copilot suggest "list all docker containers"` |
| `gh copilot explain "<command>"` | Explain a complex shell command | `gh copilot explain "ls -lrt | head -n 5"` |

## Natural Language to Shell
You can use `??` as a shortcut (if configured in your shell aliases).

-   **Find files**: `?? find all python files larger than 1MB`
-   **Git operations**: `?? undo the last commit but keep changes`
-   **Docker**: `?? stop all running containers`
-   **System info**: `?? check disk usage for current directory`

## Interactive Mode
Running `gh copilot suggest` launches an interactive mode where you can:
-   Refine the suggestion
-   Copy the command to clipboard
-   Execute the command directly

## Configuration
-   **Set default shell**: `gh copilot config`
-   **Enable data collection**: `gh copilot config` (Select "Yes" for better suggestions)

## Troubleshooting
-   If `??` doesn't work, ensure you've added the alias to your `.bashrc` or `.zshrc`.
-   Run `gh copilot alias -- help` to see installation instructions.
