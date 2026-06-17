# GitHub Onboarding

Use this guide for cohosts who need to download and update the workspace.

## Clone

```bash
git clone <private-repo-url>
cd podcast_shuo-ju-xin-li-hua
```

## Get Updates

```bash
git pull
```

Run this before starting work.

## Save Updates

```bash
git status
git add <files-you-changed>
git commit -m "Describe the update"
git push
```

## Good Commit Habits

- Commit one coherent update at a time.
- Use clear messages: `Add episode 003 brief`, `Update guest prep template`, `Revise show positioning`.
- Pull before pushing if someone else may have updated the repo.
- Ask before force-pushing or rewriting history.

## First-Time Git Identity

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## Private Repo Rule

Assume this repo contains unpublished production context. Do not make it public without a deliberate team decision.
