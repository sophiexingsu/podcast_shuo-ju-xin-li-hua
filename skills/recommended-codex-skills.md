# Recommended Codex Skills

Install skills locally on each cohost's machine. Do not copy third-party skill folders into this repo unless the team changes the policy in `context/decisions.md`.

## Install Prerequisite

Codex includes the system `skill-installer` skill. These commands assume the installer exists at the default path:

```bash
export CODEX_HOME="${CODEX_HOME:-$HOME/.codex}"
```

After installing skills, restart Codex so it can load them.

## Recommended

### transcribe

Best podcast fit. Use it to transcribe audio or video, extract text from recordings, and optionally label speakers in interviews.

Validation: official curated skill exists in `openai/skills` and supports audio transcription, diarization, and known-speaker hints.

Install:

```bash
python "$CODEX_HOME/skills/.system/skill-installer/scripts/install-skill-from-github.py" \
  --repo openai/skills \
  --path skills/.curated/transcribe
```

Use when:

- Creating transcripts from recorded episodes.
- Producing quote pulls and show notes.
- Labeling speaker turns for cohost or guest interviews.

Notes:

- Requires `OPENAI_API_KEY` for live transcription.
- Keep raw audio outside Git by default.
- Save final transcripts in each episode folder when approved.

## Optional

### speech

Use for AI-generated scratch narration, accessibility reads, internal audio drafts, or prompt samples. Do not present AI voice output as a real host or guest.

Install:

```bash
python "$CODEX_HOME/skills/.system/skill-installer/scripts/install-skill-from-github.py" \
  --repo openai/skills \
  --path skills/.curated/speech
```

### pdf

Use for media kits, sponsor one-pagers, guest packets, printable checklists, or press materials where layout matters.

Install:

```bash
python "$CODEX_HOME/skills/.system/skill-installer/scripts/install-skill-from-github.py" \
  --repo openai/skills \
  --path skills/.curated/pdf
```

### notion-knowledge-capture

Use only if the team stores production knowledge or decisions in Notion.

Install:

```bash
python "$CODEX_HOME/skills/.system/skill-installer/scripts/install-skill-from-github.py" \
  --repo openai/skills \
  --path skills/.curated/notion-knowledge-capture
```

### notion-research-documentation

Use only if the team uses Notion as the main research database.

Install:

```bash
python "$CODEX_HOME/skills/.system/skill-installer/scripts/install-skill-from-github.py" \
  --repo openai/skills \
  --path skills/.curated/notion-research-documentation
```

### jupyter-notebook

Useful later for analytics work, audience survey analysis, or sponsor reporting. It is already installed on this machine.

## Not Recommended Yet

- Deployment skills: only needed if the podcast gets a website or app.
- Figma skills: only needed if the team creates a design system or branded assets in Figma.
- Security skills: useful later if the repo grows into software or handles sensitive operational systems.
