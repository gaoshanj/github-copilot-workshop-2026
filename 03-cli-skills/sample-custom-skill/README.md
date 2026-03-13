# Sample Custom Skill: Unit Test Generator

This is a minimal example of a custom skill for GitHub Copilot.
It mocks the generation of a unit test file based on user input.

## Installation

1.  Navigate to this directory.
2.  Run `npm install` (if there were dependencies, currently none).
3.  Register this skill in VS Code (instructions vary by version, check specific documentation for "Local Skills").

## Usage

In Copilot Chat:
> `@unit-test-generator Generate tests for my login function.`

## How it works
-   `manifest.json`: Defines the skill metadata.
-   `index.js`: The script that runs when the skill is invoked. It reads JSON from `stdin` and outputs JSON to `stdout`.
