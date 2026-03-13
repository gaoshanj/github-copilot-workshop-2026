# Custom Skill Development Guide

## Overview
A Copilot Skill is a lightweight extension that adds specific capabilities to GitHub Copilot Chat. It consists of a `manifest.json` file and an entry point (usually a script or executable).

## Directory Structure
```
my-skill/
├── manifest.json       # Metadata and configuration
├── index.js            # Entry point (Node.js example)
└── package.json        # Dependencies (optional)
```

## Manifest Specification (`manifest.json`)
```json
{
  "name": "my-skill",
  "version": "1.0.0",
  "description": "Description of what the skill does",
  "commands": [
    {
      "name": "run",
      "description": "Run the skill",
      "executable": "node",
      "arguments": ["index.js"]
    }
  ]
}
```

## Input/Output
-   **Input**: The skill receives JSON input via `stdin` containing the user's prompt and context.
-   **Output**: The skill must write a JSON response to `stdout`.

## Testing
To test a skill locally:
1.  Open the Copilot Chat panel.
2.  Use the command to register a local skill (feature availability depends on VS Code version).
3.  Invoke the skill in chat: `@my-skill <prompt>`
