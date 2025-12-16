# annexstamp: Automated Legal Annex Stamping for LaTeX

**annexstamp** is a LaTeX package designed to streamline the creation of legal annexes (Anlagen). It handles the Table of Annexes, the stamping of pages (e.g., "B1", "B2"), and provides robust error handling.

## Features

- **Automated Workflow:** Just list your files; the package generates the table and includes the PDFs.
- **Auto-Configuration:** Automatically creates a data template (`annex-data.tex`) if one is missing.
- **"Safe Mode":** If a PDF file is missing or renamed, the compilation **does not crash**. Instead, it generates a visual "File Not Found" page with troubleshooting tips, allowing you to debug without halting.
- **Zero Config:** Requires only one command in your document: `\PrintAnnexes`.

## Usage

1. Copy `annexstamp.sty` to your project folder (or your local texmf tree).
2. Create a document:

```latex
\documentclass{article}
\usepackage{annexstamp}

\begin{document}
    \section{My Brief}
    See the attached evidence.
    
    % This command prints the Table of Annexes AND the stamped PDFs
    \PrintAnnexes 
\end{document}
