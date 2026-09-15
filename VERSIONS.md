# Versions

## 1.1.0 — 2026-09-15

- Add explicit Codex support across the existing 17 public skills, while preserving Claude and the Gemini/HTML routes.
- Correct project skill discovery and preserve existing installations during copy setup.
- Use each user’s profile and evidence, with accurate missing-source/provider states and no comment scraping.
- Distinguish visual prompts from generated and inspected exports.
- Add `python3 tests/test-codex-portability.py --codex` for isolated installation and live local discovery checks. Live provider access and user activation remain separate checks.

## 1.0.0 — 2026-04-22

Initial release. 17 skills covering the full content system documented in the MarTech AI newsletter.

**Voice foundation**
- voice-builder
- newsletter-voice

**LinkedIn**
- profile-optimizer
- post-writer
- graphic-designer
- post-scorer
- post-formatter
- hook-generator
- content-matrix
- niche-research
- gemini-infographic
- gemini-carousel
- quote-post

**Instagram Reels**
- reels-scripting

**YouTube**
- youtube-thumbnail

**Community**
- pinned-comment

**Analytics**
- analytics-dashboard
