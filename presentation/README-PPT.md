# Presentation Slides

The slides in this directory are written in Markdown and designed to be rendered with [Marp](https://marp.app/).

## Prerequisites

-   **VS Code**: Install the "Marp for VS Code" extension.
-   **CLI (Optional)**: If you prefer command line, install Marp CLI.

## How to View/Export

### Method 1: VS Code (Recommended)
1.  Open `slides.md` in VS Code.
2.  Open the Preview pane (Click the "Open Preview to the Side" icon).
3.  To export: Click the **Marp icon** in the editor toolbar -> **Export Slide Deck...**
4.  Choose PDF, PPTX, or HTML.

### Method 2: Command Line

1.  Install Marp CLI:
    ```bash
    npm install -g @marp-team/marp-cli
    ```

2.  Export to HTML (for web presentation):
    ```bash
    marp slides.md -o index.html
    ```

3.  Export to PPTX (requires Chrome/Edge installed):
    ```bash
    marp slides.md -o deck.pptx
    ```

4.  Export to PDF:
    ```bash
    marp slides.md -o handouts.pdf
    ```

## Theme
The slides use a custom theme defined in `theme.css`. This file must be in the same directory as `slides.md` for proper rendering.
