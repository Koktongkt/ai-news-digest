---
name: ai-news-digest
description: "Research and draft daily AI news digests across GitHub, labs, papers, and social signals."
version: 1.0.0
author: Hermes Agent
license: MIT
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [Research, News, Digest, AI, ML, Monitoring]
---

# AI News Digest

Use this skill when the user asks for a current or daily digest of AI/ML developments across multiple streams (e.g. GitHub, company/lab announcements, papers, social media).

## Core goal
Produce a concise, citation-backed digest that leads with what changed since the previous day and clearly labels weak or fragmented signal.

## Workflow

1. **Anchor the time window**
   - Use the live date/time when recency matters.
   - Prefer a 24–72 hour window unless the user asks otherwise.

2. **Split the work by stream**
   - GitHub / OSS trends
   - Big tech and AI lab announcements
   - Fresh papers
   - Social pulse (HN, Reddit, X)
   - Parallelize independent streams with delegation.
   - If there are more streams than can be done in one batch, split into multiple delegate calls rather than serializing everything.

3. **Verify before summarizing**
   - Cite every claim with a URL.
   - Prefer primary sources: official blogs, release pages, arXiv abstract pages, GitHub repos, or direct post/item URLs.
   - Do not promote a rumor, thread, or trend claim unless the source itself is inspectable.

4. **Be strict about evidence quality**
   - Distinguish:
     - official announcements
     - benchmark or infra claims
     - community chatter
   - Never turn a single social post into a settled fact.
   - If the evidence is thin, say so explicitly.

5. **Write for Telegram**
   - Use short headings and bullets.
   - Prefer small tables when comparing items.
   - Put the URL inline with each item.
   - Lead with the clearest “what changed since yesterday” summary.

## Stream-specific guidance

### GitHub / OSS
- Prefer GitHub Trending, release pages, or the repo README if it is newly prominent.
- Include the repo URL and, if relevant, the trending/release page URL.
- Do not invent star counts or momentum if the source does not support it.

### Big tech / labs
- Prefer official posts, changelogs, model cards, or newsroom items.
- Treat vendor marketing language as claims, not settled truth.
- If a post includes performance numbers, preserve the wording carefully and avoid overgeneralizing.

### Papers
- Prefer arXiv abstract pages for exact ID, date, and title.
- If the paper page is summarized or noisy, verify the abstract page directly.
- Mention when a result looks incremental, infrastructure-focused, or early-stage.

### Social pulse
- Hacker News item pages are often the best source for readable discussion.
- Reddit may be hard to scrape directly; if needed, fall back to search results plus the post URL.
- X should be treated as pulse, not proof.
- Summarize themes and skepticism, not just excitement.

## Pitfalls

- Do not fabricate citations, dates, counts, or engagement numbers.
- Do not merge official announcements and social chatter into one undifferentiated “news” bucket.
- Do not overstate a single benchmark, benchmark score, or thread as consensus.
- Do not bury signal quality; call out when the evidence is thin or fragmented.

## Output checklist

- [ ] Dates are present or clearly implied by source pages
- [ ] Every item has a URL
- [ ] What changed since yesterday is stated up front
- [ ] Signal strength is labeled when weak
- [ ] Claims are phrased conservatively

## Notes

- For current-source research, use the `arxiv` and `blogwatcher` skills when they fit the source type.
- Session-specific source patterns and verified URLs can live in `references/`.
- When a digest session surfaces unusually useful canonical URLs, query phrasing, or source-pattern recovery steps, capture them in a dated reference file under `references/` and add a one-line pointer here.

## Reference files
- `references/digest-workflow.md` — source patterns, verification notes, and a concrete fallback playbook for blocked or noisy sources.
- `references/2026-06-20-source-map.md` — verified Jun 20, 2026 source map, canonical URLs, and query patterns that worked.
