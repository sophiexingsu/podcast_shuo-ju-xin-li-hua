# Foundational Research

This note records the basis for the initial workspace structure. Update it when the team changes tools or workflow.

## Podcast Production Defaults

The initial workflow is built around a repeatable episode pipeline:

1. Topic intake.
2. Research and source gathering.
3. Episode brief.
4. Outline.
5. Recording.
6. Editing and transcript.
7. Show notes and QA.
8. Publishing and promotion.
9. Retrospective.

This is reflected in `docs/production-workflow.md`, `episodes/_template/`, and `templates/`.

## Skill Research

The official curated Codex skill list was checked through the local `skill-installer` helper. Relevant available skills:

- `transcribe`: validated as the best fit for podcast production because it supports audio/video transcription, optional speaker diarization, and known-speaker hints.
- `speech`: useful for AI-generated scratch narration, accessibility reads, or internal audio drafts. It requires clear disclosure if used externally.
- `pdf`: useful for media kits, guest packets, sponsor sheets, and printable documents where layout matters.
- `notion-knowledge-capture`: useful only if the team uses Notion as a knowledge base.
- `notion-research-documentation`: useful only if the team uses Notion for research documentation.
- `jupyter-notebook`: useful later for analytics or survey analysis, but not required for basic production.

## Validation Notes

- The OpenAI curated skill catalog was queried locally with:

  ```bash
  python "$HOME/.codex/skills/.system/skill-installer/scripts/list-skills.py" --format json
  ```

- The `transcribe`, `speech`, and `pdf` skill descriptions were checked from the official `openai/skills` repository.
- The external podcast workflow references below were checked for current production themes: clear workflow, launch planning, repeatable production stages, publishing, and promotion.

## Sources

- OpenAI skills repository: `https://github.com/openai/skills`
- OpenAI curated `transcribe` skill: `https://raw.githubusercontent.com/openai/skills/main/skills/.curated/transcribe/SKILL.md`
- OpenAI curated `speech` skill: `https://raw.githubusercontent.com/openai/skills/main/skills/.curated/speech/SKILL.md`
- OpenAI curated `pdf` skill: `https://raw.githubusercontent.com/openai/skills/main/skills/.curated/pdf/SKILL.md`
- Podcast workflow reference: `https://www.epodcastproductions.com/podcasting-blog/podcasting-made-easy-how-a-workflow-can-simplify-your-production-process`
- Podcast launch checklist reference: `https://contentallies.com/learn/podcast-launch-checklist`
