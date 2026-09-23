# Job Scout

Job Scout helps an AI assistant find, verify, summarize, and compare public job postings.

This starter has no bundled job database, custom API, account, or credential. It uses the web search or browser tools available in the host AI assistant. Search coverage and page access depend on that host and on what each source makes public.

## Requirements

- An AI assistant that supports `SKILL.md` skills
- Public web search or browser access in that assistant

Without search or browser access, the assistant can still analyze job links that the user provides, but it cannot discover new listings.

Job Scout does not require a service account or API token. The host AI service may have separate usage limits or charges.

## Install in Codex

Copy the complete `job-scout` folder into:

- `$CODEX_HOME/skills/job-scout`, when `CODEX_HOME` is set; or
- `~/.codex/skills/job-scout`, otherwise.

Reload the skill list or restart Codex if needed. For other AI assistants, follow their skill installation process and confirm they have public search or browser access.

## Try it

```text
Use $job-scout to find AI product internships in Ningbo. Give me the original posting links and summarize each role's requirements.
```

The skill reports source links and verification limits. It does not apply to jobs, contact recruiters, save a resume, or upload personal details.

## Before public distribution

Choose a license if you want to grant others permission to reuse or modify this repository. Review the supported skill format and web-search capabilities of the target assistant.
