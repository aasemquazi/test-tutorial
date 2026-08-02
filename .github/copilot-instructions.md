Copilot instructions for this repository

1) Build, test, and lint commands
- None detected in the repository root: no package.json, requirements.txt, Makefile, or other CI scripts were found.
- If build/test tooling is added later, prefer documenting the exact commands in README or package.json scripts. Example single-test invocations to include when present:
  - Node (jest): npm test -- -t "<test name or pattern>"
  - Python (pytest): pytest -k "<expr>" <path/to/test.py>::<TestClass>::<test_method>
  - Make: make test TEST=<single-test-target>

2) High-level architecture / big picture
- This repository currently contains small tutorial artifacts (plain text and minimal code snippets) and a single GitHub Action file.
  - newcode/ and code-second/ — ad-hoc code/content directories (each contains small plain-text code snippets).
  - configs/custom-conifg — repository configuration files (note: folder name contains a likely typo: "custom-conifg").
  - .github/workflow/first-workflow — a simple GitHub Actions workflow that echoes messages.
- There is no language-specific project structure, dependency manifest, or test harness. As the repo grows, expect typical roots such as package.json, pyproject.toml/requirements.txt, Cargo.toml, or a Makefile to indicate how to build/test/lint.

3) Key conventions and repository-specific notes (important for automated assistants)
- Non-standard workflow directory: GitHub's conventional workflows directory is .github/workflows (plural). This repo uses .github\workflow (singular). Copilot should look in both locations when searching for CI files and flag the discrepancy when suggesting CI changes.
- Misspelled config directory: configs\custom-conifg appears to be intended as custom-config. Avoid automated renames without human confirmation; surface this to maintainers.
- File types: many repository files are plain text (e.g., xyz.txt, abcd.txt). When proposing language-specific fixes, verify the file is actually source code and identify the intended language first.
- When suggesting new tests, tooling, or CI changes, reference explicit manifests (package.json, pyproject.toml, requirements.txt, Makefile) rather than assuming a language.
- Minimal CI present: the existing .github workflow is a basic echo script; Copilot should not assume tests run in CI until a test step is present.

4) Files checked for AI assistant configs
- Searched for common assistant configuration files and did not find: CLAUDE.md, .cursorrules, .cursor/rules/, AGENTS.md, .windsurfrules, CONVENTIONS.md, AIDER_CONVENTIONS.md, .clinerules, .cline_rules.

What was created
- Added: .github/copilot-instructions.md (this file) containing the above summary and pointers.

Questions
- Would you like Copilot instructions expanded to include example CI/test templates for a specific language (Node/Python/Java/Rust) or to configure an MCP server relevant to the project?