# Commit Message Generator

## Objective
Produce a clear, informative commit message for a set of code changes, following best practices or a specified format (e.g., Conventional Commits).

## Context to Provide
- `{{project_description}}` – context of the changes (what feature/bug is addressed)
- `{{repository_link}}` – (optional) link to or excerpt of the code diff (you may also paste the diff directly)
- `{{additional_constraints}}` – e.g. commit message style guidelines (prefixes like feat/fix, line length, referencing issue IDs)
- `{{desired_output_format}}` – default: Markdown (commit message can be formatted in a code block or plain text)

## AI Steps
1. Summarize the provided changes, identifying key components or functionalities affected
2. Determine an appropriate commit type or prefix if using a convention (e.g., "feat:", "fix:") based on the nature of the changes
3. Draft a short, imperative summary line (ideally under 50 characters) describing the change
4. If more detail is needed, add a body below: explain what was changed and why, possibly as a brief paragraph or bullet list of notable changes. Include issue/ticket references if provided
5. Ensure the final message meets formatting rules (wrapping, punctuation) and clearly communicates the purpose of the commit

## Output Specification
A properly formatted commit message. For example:

```
feat: add password reset feature

Adds endpoint, email template, and tests for password reset functionality.

Closes #123
```

If a single-line message is sufficient, just output that. Follow any given style rules (e.g., capitalization, mood, metadata).

## Hallucination Guards
- Use only information from the provided diff/description—do not introduce changes or reasons not present
- If the change context is unclear or incomplete, ask for clarification instead of guessing
- Do not include issue IDs or links unless they were provided
- If uncertain about any detail, get confirmation rather than including it in the commit message

## Adaptation Note
Adjust the format for different conventions or VCS systems as needed (e.g., no prefix for teams not using Conventional Commits, or including additional metadata for certain projects). Always adhere to project-specific guidelines for tone and structure.

## Default Tech Stack
TypeScript + React + Node/Nest
