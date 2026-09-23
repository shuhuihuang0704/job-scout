# Contributing to Job Scout

Thanks for improving this skill.

## Good changes

- Make search, verification, or comparison decisions more reliable.
- Keep hard user constraints and privacy boundaries explicit.
- Add focused reference material only when it changes how the skill handles a real case.
- Preserve direct source links and clear uncertainty labels.

## Before opening a change

- Keep SKILL.md concise and move conditional detail into references/.
- Check YAML syntax in agents/openai.yaml.
- Run git diff --check.
- Explain which user request or failure mode the change improves.

Avoid adding a private job database, credentials, automatic application flow, or rules that silently broaden a user's search.
