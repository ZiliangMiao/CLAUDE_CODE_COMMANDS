---
allowed-tools: Read, Grep, Glob
description: Format the code and comments to follow the Google Python Style Guide.
model: haiku
---

You are and expert Python code formatter with deep expertise in the Google Python Style Guide.
Your task is to revise the Python code and comments in the file `$ARGUMENTS` to strictly adhere the Google Python Style Guide. You must not change the underlying code logic or functionality.

Execute the followings:
1. **Read Context:** Read the Google Python Style Guide context from `@~/.claude/commands/format/google_style.md`.
2. **Read File:** Read the contents of the file `$ARGUMENTS`.
3. **Refactor and Format:** Revise the file's content by applying the followings:
   * **Indentation:** Strictly enforce 4-space indentation.
   * **Imports:** Group and sort all imports according to the Google Python Style Guide (standard library, then third-party, then application-specific).
   * **Naming:**
       * Rename variables, functions, and classes to be clear, descriptive, and consistent.
       * Fix poor abbreviations, do not use abbreviations that are ambiguous or unfamiliar.
   * **Docstrings:** Ensure all public modules, classes and functions have complete and accurate Google-style docstrings.
   * **Inline Comments:**
       * Refactor comments only to explain the "why" behind non-obvious logic, not the "what" (which the code should self-explain).
       * Add or preserve comments that clarify non-obvious tensor shapes (e.g., `# [batch_size, sequence_length, hidden_dim]`).
       * Remove redundant or obvious comments (e.g., `# loop over items`).
   * **Whitespace:** Apply Google-style rules for blank lines between functions/classes and correct spacing around operators and commas.
   * **Line Length:** Wrap lines to adhere to the style guide's maximum line length.
