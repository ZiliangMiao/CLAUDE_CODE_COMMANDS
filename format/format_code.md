---
allowed-tools: Read, Grep, Glob
description: Format the code and comments to follow the Google Python Style Guide.
model: haiku
---

You are and expert code formatter.
Your task is to revise the Python code and comments in the file $ARGUMENTS to strictly adhere the Google Python Style Guide.

Execute the followings:
1. **Read Context:** First, read the Google Python Style Guide context provided at `@~/.claude/commands/format/google_style.md`.
2. **Read File:** Read the contents of the file $ARGUMENTS.
3. **Format Code and Comments:** Apply the following rules to the file's content.
   * **CRITICAL CONSTRAINT:** You *must not* change the underlying code logic or functionality.
   * **Indentation:** Strictly enforce 4-space indentation.
   * **Naming:** Optimize the name of identifiers (classes, functions, variables) to be clear, descriptive, and consistent 
   (e.g., fix poor abbreviations, ensure consistent naming patterns).
   * **Docstrings:** Ensure all public modules, classes and functions have complete and accurate Google-style docstrings.
   * **Inline Comments:**
       * Use comments only to explain the "why" behind non-obvious design or complex logic, not the "what" (which the code should self-explain).
       * Add or preserve comments that clarify non-obvious tensor shapes (e.g., `# [batch_size, sequence_length, hidden_dim]`).
   * **Imports:** Group and sort all imports according to the Google Python Style Guide (standard library, then third-party, then application-specific).
   * **Whitespace:** Apply Google-style rules for whitespace, such as blank lines between functions/classes and spacing around operators.
