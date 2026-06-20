# ai-news-digest

A Hermes skill for researching and drafting a daily AI/ML news digest.

## What it does

Use this skill when you want a concise, citation-backed summary of what changed in AI since the previous day across four streams:

- GitHub / OSS trends
- Big tech and AI lab announcements
- Fresh research papers
- Social pulse from Hacker News, Reddit, and X

## Writing goals

- Lead with the clearest "what changed since yesterday" summary
- Cite every claim with a URL
- Prefer primary sources
- Flag weak, thin, or fragmented signal instead of overstating it
- Keep the output readable for Telegram

## Included files

- `SKILL.md` — main skill instructions and workflow
- `references/digest-workflow.md` — reusable source patterns and fallback playbook
- `references/2026-06-20-source-map.md` — verified canonical URLs and query patterns from a sample digest run

## Typical output shape

The skill is designed to produce a short, structured digest with URLs inline and separate sections for:

- headline changes
- official announcements
- papers
- social / OSS pulse

## Notes

This repo is meant to be a reusable research skill, not a single finished digest.
