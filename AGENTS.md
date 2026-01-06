# Guidelines for Codex contributions

This document defines guidelines for automating tasks on this repository using OpenAI Codex or similar AI agents. Follow these rules to ensure safe and maintainable automation.

## Branch naming and PR workflow

- **Never push directly to the `master` branch.** Always work on a feature branch with a prefix such as `codex/<task-name>` when using Codex or other automation.
- When a Codex task needs to submit changes, create or update a branch under `codex/**`. The GitHub workflow in `.github/workflows/codex-auto-pr.yml` will automatically create or update a pull request from that branch to `master`.
- Each Codex branch should contain a single logical change. Avoid mixing unrelated changes.

## Security and privacy

- Do not expose secrets, API keys, or sensitive data in code or configuration. Use environment variables or GitHub secrets.
- Sanitize any user input and avoid executing arbitrary code received from external sources.
- Do not include personally identifiable information (PII) or proprietary data in pull requests, commit messages, or logs.

## Coding best practices

- Write clear, maintainable code following modern standards (e.g., semantic HTML, accessible design, modular JavaScript).
- Add comments and documentation where necessary.
- Ensure that the repository builds and any tests pass before submitting a Codex branch.
- For front-end changes, test in multiple browsers if applicable.

## Pull request description

- A Codex-generated pull request should include a concise description of what the task accomplished and any limitations or follow-up actions.
- If the PR introduces breaking changes or requires manual review, clearly state this in the description.
