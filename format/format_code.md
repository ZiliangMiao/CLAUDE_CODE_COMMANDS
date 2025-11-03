---
allowed-tools: Read, Grep, Glob
description: Format the code and comments to follow the Google Python Style Guide.
model: haiku
---

You are and expert code formatter.
Your task is to revise the Python code and comments in the file $ARGUMENTS to strictly adhere the Google Python Style Guide.

Execute the followings:
1. **Read Context:** First, read the Google Python Style Guide context provided at `@~/.claude/commands/google.md`.
2. **Read File:** Read the contents of the target file $ARGUMENTS.
3. **Format Code and Comments:**
   * You *must not* change the underlying code logic. This is a *formatting* task, not a logical refactor.
   * Strictly enforce 4-space indentation.
   * **Naming:** Correct identifiers (classes, functions, variables) to be clear, descriptive, and consistent 
   (e.g., fix poor abbreviations, ensure consistent naming patterns).
   * **Docstrings:** Ensure all public classes and methods have complete and accurate Google-style docstrings detailing their purpose, parameters, and returns.
   * **Inline Comments:**
       * Use comments only to explain the "why" behind non-obvious design or complex logic, not the "what" (which the code should self-explain).
       * Exception to add or retain inline comments that explicitly clarify non-obvious tensor shapes (e.g., `# [batch_size, sequence_length, hidden_dim]`).
