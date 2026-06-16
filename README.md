# Underpaid Overeduated Podcast Workspace

Private production workspace for planning, recording, editing, publishing, and improving the podcast.

This repo is meant to be cloned by all cohosts so everyone shares the same context, templates, decisions, and Codex skill guidance.

## Podcast Description

`高知不高值` 是一档由两个北美博士后主持的半认真对谈播客。我们聊 AI、认知科学、心理学和普通生活，但不急着把它们变成自我提升工具、效率方法论或职场生产力。

两位主播都曾在顶尖学术范式里受训，也都从那里毕业离场；我们懂那些通往“优秀”的路径，却并不觉得自己属于社会意义上的前 1%。比起成为更高效的劳动者，我们更关心如何让生活重新流动起来，如何保留好奇、幽默、创造力和一点不合时宜的希望。

这里不提供成功学公式，也不教你如何成为 AI 时代最不可替代的人。我们只是想把知识拿来玩，拿来想象，拿来讨论失败、关系、荒诞感和普通人的精神出路。

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
