# AGENTS.md

This repository supports the ESIIL oxygen on coral reefs project and its public MkDocs website.

Guidelines for agents:

- Treat the repository as the source of truth.
- Treat the website as a rendered view of repository state.
- Make small, focused edits. Avoid rewriting entire files unless the file is stale template content.
- Preserve project-specific science, data, meeting notes, and historical context unless explicitly instructed.
- Do not perform destructive rewrites.
- Prefer improving shared systems over one-off fixes.
- Keep documentation synchronized with repository structure.
- Keep documentation and site content in sync.
- Do not introduce complex HTML into Markdown pages.
- Keep everything editable by non-experts in GitHub.
- Do not add blocking tests for template completeness. Use the site health report for user-facing warnings instead.
- After meaningful changes, append an entry to `PROMPT_ACTION_LOG.md`.

OASIS template guidance:

- This repository borrows current infrastructure from `CU-ESIIL/Working_group_OASIS`, but it is a project repository for dissolved oxygen and coral reef ecology.
- Adapt working-group language where needed so it fits this project lifecycle.
- Keep participant-editable content in Markdown.
- Keep large data out of GitHub when it belongs in persistent storage; document where it lives instead.
- Preserve process galleries, image slots, meeting-note templates, site-health checks, and prompt logs.
