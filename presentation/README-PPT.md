# GitHub Copilot Workshop Presentation Guide

This directory contains the source code for the "GitHub Copilot Deep Dive Workshop" presentation slides.

## Prerequisites

To build or view these slides, you need:

1.  **VS Code**: [Download](https://code.visualstudio.com/)
2.  **Marp for VS Code Extension**: [Install from Marketplace](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)
3.  **Node.js (Optional)**: For CLI export.

## How to View

1.  Open `presentation/slides.md` in VS Code.
2.  Click the **Open Preview to the Side** icon in the editor toolbar (or press `Ctrl+K V`).
3.  You will see the rendered slides with the GitHub Dark theme.

## How to Export

### Method 1: VS Code Extension (Recommended)

1.  Open `presentation/slides.md`.
2.  Click the **Marp** icon in the editor toolbar (it looks like a triangle).
3.  Select **Export Slide Deck...**.
4.  Choose your format:
    *   **PDF**: Best for sharing.
    *   **PowerPoint (.pptx)**: Best for presenting (note: some CSS/Mermaid might require adjustments in PPT).
    *   **HTML**: Interactive web presentation.

### Method 2: Marp CLI

If you prefer command line or CI/CD generation:

1.  Install Marp CLI:
    ```bash
    npm install -g @marp-team/marp-cli
    ```

2.  Export to PDF:
    ```bash
    marp presentation/slides.md --pdf --allow-local-files -o presentation/slides.pdf
    ```

3.  Export to PPTX:
    ```bash
    marp presentation/slides.md --pptx --allow-local-files -o presentation/slides.pptx
    ```

## Customization

*   **Theme**: The slides use a custom GitHub Dark theme defined in the frontmatter of `slides.md`. You can adjust the `style` block to change colors or fonts.
*   **Mermaid**: Diagrams are rendered using Mermaid.js. Ensure `mermaid: true` is set in the frontmatter.

## Speaker Notes

Speaker notes are embedded in the markdown using `<!-- speaker_note: ... -->`. You can view them in "Presenter Mode" when exporting to HTML or using the VS Code preview.
