# 说句心里话 Podcast Workspace

Private production workspace for planning, recording, editing, publishing, and improving the podcast.

This repo is meant to be cloned by all cohosts so everyone shares the same context, templates, decisions, and Codex skill guidance.

## Podcast Description

`说句心里话` 是一档从真实感受出发的半认真对谈播客。我们可以从一场演唱会、一段追星经历、一条热搜或一个日常尴尬聊起，也可以一路聊到 AI、认知科学、心理学、公共议题和严肃科学问题。

我们关心流行文化和饭圈文化里的情绪、关系、身份和权力，也关心科学知识如何改变我们理解世界的方式。话题可以轻，也可以重；可以很好笑，也可以很认真。重要的是不急着给标准答案，而是把那些想了很久、但平时不一定说出口的话讲清楚。

这里不是学术讲座，也不是情绪树洞。我们想用一点好奇心、批判性和幽默感，把生活里看似不相干的东西连起来：喜欢什么、相信什么、为什么生气、为什么被打动，以及我们如何在复杂世界里继续保持判断和感受。

## Quick Start

1. Clone the private GitHub repo:

   ```bash
   git clone <private-repo-url>
   cd podcast_shuo-ju-xin-li-hua
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
