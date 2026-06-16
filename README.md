# Underpaid Overeduated Podcast Workspace

Private production workspace for planning, recording, editing, publishing, and improving the podcast.

This repo is meant to be cloned by all cohosts so everyone shares the same context, templates, decisions, and Codex skill guidance.

## Quick Start

1. Clone the private GitHub repo:

   ```bash
   git clone <private-repo-url>
   cd podcast_Underpaid_Overeduated
   ```

2. Read the shared context:

   ```bash
   open context/show-bible.md
   open docs/production-workflow.md
   open skills/recommended-codex-skills.md
   ```

3. Install recommended Codex skills locally. Start with `transcribe`:

   ```bash
   python "$HOME/.codex/skills/.system/skill-installer/scripts/install-skill-from-github.py" \
     --repo openai/skills \
     --path skills/.curated/transcribe
   ```

4. Start a new episode by copying the template folder:

   ```bash
   cp -R episodes/_template "episodes/001-working-title"
   ```

5. Commit small updates as the work changes:

   ```bash
   git status
   git add README.md context docs episodes templates skills
   git commit -m "Update podcast workspace"
   git push
   ```

## Repo Map

- `context/`: durable show context, audience notes, decisions, glossary, and topic backlog.
- `docs/`: workflow, onboarding, privacy, naming, research, and collaboration rules.
- `episodes/`: per-episode briefs, outlines, transcripts, notes, and publishing checklists.
- `templates/`: reusable briefs, checklists, and production documents.
- `skills/`: recommended local Codex skills and validation notes.

## Privacy Defaults

Use a private GitHub repo. Do not commit credentials, raw unreleased recordings, private guest contact details, ad account data, or API keys. See `docs/privacy-rules.md`.

## Current Setup State

This workspace is foundational. The show concept, format, audience, cadence, and brand voice should be filled in next in `context/show-bible.md`.
