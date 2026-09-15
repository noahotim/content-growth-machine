<p align="center">
  <img src="assets/banner.svg" alt="Content Growth Machine" width="100%"/>
</p>

# Content Growth Machine

**17 standalone social media skills for OpenCode, Claude & Codex** — voice, LinkedIn writing, research, analytics, Reel scripting and Gemini image prompts. Ported from [charlie947/social-media-skills](https://github.com/charlie947/social-media-skills) (3.5k stars) for OpenCode.

Built by [Charlie Hills](https://charliehills.substack.com) — original system behind 415k+ followers, 100M+ views/year. OpenCode port by [noahotim](https://github.com/noahotim).

## What is this?

Agent Skills that turn OpenCode into a complete content growth machine:

* **Writes posts, hooks, ideas, and remixes in your own voice** using your past top-performing content
* **Learns from performance data** to create better content for LinkedIn, Instagram, X, and YouTube
* Voice foundation (`voice-builder`) → every other skill reads `about-me.md` + `voice.md`

```
                    ┌──────────────────────────────────────┐
                    │           voice-builder              │
                    │   about-me.md + voice.md             │
                    └──────────────────┬───────────────────┘
                                       │
                    ┌──────────────────▼───────────────────┐
                    │         newsletter-voice             │
                    └──────────────────┬───────────────────┘
                                       │
     ┌────────────┬────────────┬───────┴───────┬────────────┬────────────┐
     ▼            ▼            ▼               ▼            ▼            ▼
┌──────────┐ ┌──────────┐ ┌──────────┐ ┌──────────────┐ ┌──────────┐ ┌──────────┐
│ Profile  │ │LinkedIn  │ │ Video    │ │ Analytics &  │ │Community │ │Standalone│
└──────────┘ └──────────┘ └──────────┘ └──────────────┘ └──────────┘ └──────────┘
```

## Available Skills (17)

| Skill | Description |
|---|---|
| [voice-builder](skills/voice-builder/) | Build `about-me.md` + `voice.md` from interview + 3-5 samples. Foundation. |
| [newsletter-voice](skills/newsletter-voice/) | Newsletter-specific rules on top of voice-builder |
| [profile-optimizer](skills/profile-optimizer/) | Rebuild LinkedIn profile for conversions + 4 image prompts |
| [post-writer](skills/post-writer/) | Draft LinkedIn posts in your voice |
| [graphic-designer](skills/graphic-designer/) | HTML/CSS + PNG or Gemini image prompt |
| [post-scorer](skills/post-scorer/) | Score draft vs your history (Apify optional) |
| [reels-scripting](skills/reels-scripting/) | Reel analysis via Apify+Gemini, draft in your voice |
| [youtube-thumbnail](skills/youtube-thumbnail/) | Title → branded Gemini thumbnail prompt |
| [pinned-comment](skills/pinned-comment/) | Meme pinned comment + image prompt |
| [hook-generator](skills/hook-generator/) | 6 hook angles from your facts |
| [post-formatter](skills/post-formatter/) | PAS/AIDA/BAB/STAR/SLAY formatter |
| [content-matrix](skills/content-matrix/) | 3-5 pillars × 8 formats = 24-40 ideas |
| [niche-research](skills/niche-research/) | 20 dated stories from last 7 days |
| [gemini-infographic](skills/gemini-infographic/) | Whiteboard infographic brief |
| [gemini-carousel](skills/gemini-carousel/) | Carousel per-slide Gemini prompts |
| [quote-post](skills/quote-post/) | Original quotes + Gemini prompt |
| [analytics-dashboard](skills/analytics-dashboard/) | LinkedIn export → React dashboard + 5 recommendations |

## Installation

### OpenCode (this repo - recommended)

OpenCode discovers skills at these paths:
- `.opencode/skills/<name>/SKILL.md` (project)
- `~/.config/opencode/skills/<name>/SKILL.md` (global)
- `.claude/skills/` / `.agents/skills/` (also discovered)

**Option A: Clone this repo and copy (works everywhere)**

```bash
git clone https://github.com/noahotim/content-growth-machine.git
# project-local (this project only)
mkdir -p .opencode/skills
cp -R content-growth-machine/skills/* .opencode/skills/

# global (all projects)
mkdir -p ~/.config/opencode/skills
cp -R content-growth-machine/skills/* ~/.config/opencode/skills/
```

**Option B: Use directly from this repo path**

This repo already contains `.opencode/skills/`, `.agents/skills/`, `.claude/skills/` pre-populated. Clone it as your content project and skills are discovered automatically.

**Verify:**
```bash
ls .opencode/skills/voice-builder/SKILL.md
ls ~/.config/opencode/skills/voice-builder/SKILL.md
```

Then in OpenCode, call:
```
skill({ name: "voice-builder" })
skill({ name: "post-writer" })
```

### Claude Code

```text
/plugin marketplace add noahotim/content-growth-machine
/plugin install content-growth-machine
# or original: /plugin marketplace add charlie947/social-media-skills
```

### Codex

```bash
git clone https://github.com/noahotim/content-growth-machine.git
mkdir -p .agents/skills
for skill in content-growth-machine/skills/*; do
  [ -f "$skill/SKILL.md" ] || continue
  name="$(basename "$skill")"
  [ -e ".agents/skills/$name" ] || cp -R "$skill" ".agents/skills/$name"
done
```

## Usage

**1. Build voice first (required for personalization):**

```
"Build my voice" → voice-builder
"Learn my voice" → voice-builder
```

Creates `about-me.md` + `voice.md` in project root. Every other skill reads these.

**2. Then create:**

```
"Write me a post about AI agents" → post-writer
"Score this draft against my history" → post-scorer
"Make me a carousel from this" → gemini-carousel
"What should I post this week" → niche-research or content-matrix
"Turn this outlier Reel into a script" → reels-scripting
"I need a thumbnail for 'How I fired my team'" → youtube-thumbnail
"Write me a pinned comment" → pinned-comment
"Give me 6 hooks for this topic" → hook-generator
```

## OpenCode Example

```bash
opencode run "Build my voice - I'm a founder writing for founders about AI and growth"
# then
opencode run "Write a LinkedIn post about why I automated my content system - use my voice"
```

## Credits

* Original skills: [charlie947/social-media-skills](https://github.com/charlie947/social-media-skills) by Charlie Hills — MIT License
* OpenCode port maintains 100% compatibility with Claude/Codex originals. Added `.opencode/skills/` discovery.
* Upstream: 3.5k stars, 815 forks, v1.1.0

## License

[MIT](LICENSE) — same as upstream. If it helps you, link back to [Charlie's newsletter](https://charliehills.substack.com).

## Contributing

PRs welcome. Run `bash validate-skills.sh` and `python3 tests/test-codex-portability.py` before submitting.
