# Contributing to Job Scout

Thanks for improving this skill.

## Good changes

- Make search, verification, or comparison decisions more reliable.
- Keep hard user constraints and privacy boundaries explicit.
- Preserve direct source links and clear uncertainty labels.
- Improve installation, discoverability, or maintenance without adding unrelated scope.

## Workflow

1. Start from a concrete user request, observed failure, or documentation gap.
2. Keep core decision rules in `SKILL.md`; put conditional detail in the smallest relevant reference.
3. Update the README when an installation path, supported workflow, or public limitation changes.
4. Use a focused commit or pull request description that explains the behavior being improved.

## Before opening a change

- Keep `SKILL.md` concise and move conditional detail into `references/`.
- Check YAML syntax in `agents/openai.yaml`.
- Run `git diff --check`.
- Check that every reference linked from `SKILL.md` exists.
- Make sure examples do not promise private data, exhaustive coverage, or automatic applications.
- If the installation layout changes, verify a fresh clone contains `SKILL.md`, `agents/`, `references/`, and `LICENSE`.

Avoid adding a private job database, credentials, automatic application flow, or rules that silently broaden a user's search.
