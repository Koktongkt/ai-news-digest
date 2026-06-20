# AI News Digest — working notes

Session-specific notes and reusable research patterns for daily AI digests.

## Verified source patterns from 2026-06-15

### Official announcements
- OpenAI Partner Network: https://openai.com/index/introducing-openai-partner-network/
- OpenAI Academy courses: https://openai.com/index/academy-courses-applying-ai-at-work/
- Anthropic access suspension: https://www.anthropic.com/news/fable-mythos-access
- Meta accessibility glasses program: https://about.fb.com/news/2026/06/free-ai-glasses-for-every-blind-veteran/
- NVIDIA AgentPerf / Blackwell: https://blogs.nvidia.com/blog/nvidia-blackwell-agentperf-artificial-analysis/

### Papers verified on arXiv abstract pages
- https://arxiv.org/abs/2606.14516
- https://arxiv.org/abs/2606.14571
- https://arxiv.org/abs/2606.14694
- https://arxiv.org/abs/2606.14667
- https://arxiv.org/abs/2606.14703

### Social pulse sources that worked well
- Hacker News item pages were directly readable and provided the clearest discussion signal.
- Reddit direct extraction failed on the sampled LocalLLaMA posts; use `web_search` to locate the post URL, then cite the post URL and the search snippet if direct scraping is blocked.
- X public post URLs were usable via search results; treat them as pulse, not proof.

## Fallback playbook

1. If a source page blocks extraction, use `web_search` to recover the canonical URL.
2. If direct content is still inaccessible, cite only what the search snippet or item page explicitly shows.
3. If evidence is thin, say: "signal is thin" or "fragmented signal".
4. Keep official announcements, paper abstracts, and social chatter in separate subsections.

## Writing notes

- Start with the change since yesterday.
- Use short bullets with URLs inline.
- Avoid engagement-count claims unless the source page itself exposes them and they matter.
- Phrase performance or benchmark claims conservatively.
