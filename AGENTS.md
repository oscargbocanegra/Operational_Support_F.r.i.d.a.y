# Repository Guidelines

## Project Structure & Module Organization

This repository is currently a clean starting point: no source, test, asset, or build directories are present yet. Keep the root focused on project metadata and documentation. As implementation begins, use a conventional layout such as `src/` for production code, `tests/` for automated tests, and `assets/` for static resources. Keep modules grouped by feature rather than by framework layer when practical.

## Build, Test, and Development Commands

No build system or development scripts are configured yet. Before adding a new toolchain, document its canonical commands here and in the project README. At minimum, provide commands for:

```text
build   # produce a release or distributable artifact
test    # run the complete automated test suite
lint    # check style and static-analysis rules
dev     # start the local development workflow
```

Prefer repository-local scripts (for example, `npm test` or `make test`) so contributors use the same tool versions and options.

## Coding Style & Naming Conventions

Follow the formatter and linter selected for the project; do not rely on editor-specific formatting. Use four spaces for Markdown indentation, clear feature-oriented names, and consistent casing: `PascalCase` for types/classes, `camelCase` for functions and variables, and `UPPER_SNAKE_CASE` for constants. Keep public APIs small and document non-obvious decisions.

## Testing Guidelines

Add tests alongside each new behavior under `tests/` (or the language-standard test location once a stack is selected). Name tests after the behavior they verify, such as `rejects_invalid_configuration`. Every change should include focused tests and pass the full suite before review. Record coverage expectations when the test framework is introduced.

## Commit & Pull Request Guidelines

Use short, imperative commit subjects, preferably in Conventional Commits form (for example, `feat: add configuration loader` or `docs: update contributor guide`). Keep commits focused. Pull requests should explain the motivation, summarize the implementation, list verification commands and results, link related issues, and include screenshots or sample output when behavior is user-visible.

## Security & Configuration

Never commit credentials, tokens, generated secrets, or machine-specific configuration. Add safe defaults and document required environment variables with placeholder values. Review generated files and dependency changes before committing.
