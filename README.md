# CreatorSkills Free Skills

Free [Agent Skills](https://www.anthropic.com/news/skills) for content creators — YouTube, podcasting, newsletters, and social, in the open `SKILL.md` format used by Claude Code, Claude.ai, Cursor, and other agent runtimes.

These are the skills [CreatorSkills](https://creatorskills.co) gives away for free, published here as plain source files under the MIT license so they can be reviewed, forked, and used outside the marketplace. CreatorSkills also sells a larger paid catalog of skills and multi-file packs at [creatorskills.co](https://creatorskills.co) — none of that paid content is in this repo.

## Skills

| Skill | What it does |
| --- | --- |
| [Blog Post Outline Generator](skills/blog-post-outline-generator/SKILL.md) | Turn a rough topic into a structured blog outline with titles, H2/H3 flow, proof ideas, and CTAs — ready to draft in minutes. |
| [Community Post Ideas](skills/community-post-ideas/SKILL.md) | 30 days of YouTube Community tab ideas — polls, questions, updates — written so your audience actually clicks instead of scrolling past. |
| [Content Idea Brainstormer](skills/content-idea-brainstormer/SKILL.md) | Never stare at a blank upload schedule again — get 10 specific, ready-to-film content ideas for any niche in seconds. |
| [Content Repurposing Planner](skills/content-repurposing-planner/SKILL.md) | Paste your YouTube video or podcast and get a full repurposing plan: which clips to extract, where to post them, and why. |
| [Creator Bio Generator](skills/creator-bio-generator/SKILL.md) | Platform-optimized bios for YouTube, Instagram, TikTok, Twitter, and LinkedIn — all from a single input. |
| [Creator Productivity Second Brain](skills/creator-productivity-second-brain/SKILL.md) | A personal productivity system for creators — goal tracking, project management, time blocking, and content planning in one connected workspace. |
| [Email Subject Line Optimizer](skills/email-subject-line-optimizer/SKILL.md) | Generate 5 high-converting email subject lines instantly — built for newsletters and creator announcements that earn the open. |
| [Instagram Reels Script Writer](skills/instagram-reels-script-writer/SKILL.md) | Shot-ready Reels scripts in 15, 30, 60, or 90 seconds — with hook, body, CTA, caption, and audio suggestions. |
| [KDP Self-Publishing Launch Kit](skills/kdp-self-publishing-launch-kit/SKILL.md) | Plan, research, and launch a Kindle Direct Publishing book — from niche validation to cover brief to launch week marketing calendar. |
| [LinkedIn Post Formatter](skills/linkedin-post-formatter/SKILL.md) | Turn rough ideas into polished LinkedIn posts with stronger hooks, cleaner structure, and engagement-ready CTAs. |
| [Newsletter Subscriber Growth Engine](skills/newsletter-subscriber-growth-engine/SKILL.md) | Diagnose growth blockers, build a lead magnet, convert followers to subscribers, land cross-promos, and write a welcome email that retains people. |
| [Podcast Show Notes Creator](skills/podcast-show-notes-creator/SKILL.md) | Drop in your transcript or outline and get SEO-optimized show notes, timestamps, key quotes, and social captions. |
| [Post-to-Thread Converter](skills/post-to-thread-converter/SKILL.md) | Turn any blog post, newsletter, or brain dump into a Twitter thread and a LinkedIn post. |
| [TikTok Script Template](skills/tiktok-script-template/SKILL.md) | Generate TikTok-native scripts with better hooks, pacing, and comment-focused CTAs. |
| [YouTube Chapter Generator](skills/youtube-chapter-generator/SKILL.md) | Turn a transcript into timestamped YouTube chapters that boost retention and search visibility. |
| [YouTube to Twitter Thread](skills/youtube-to-twitter-thread/SKILL.md) | Paste a YouTube link or transcript, get back a ready-to-post Twitter/X thread that pulls out the best moments. |
| [YouTube Video Description Writer](skills/youtube-video-description-writer/SKILL.md) | Generate publish-ready YouTube descriptions, with better keyword coverage and stronger viewer CTAs. |

Each skill folder contains:

- `SKILL.md` — the skill itself (YAML frontmatter + instructions), in the open Agent Skills format
- `README.md` — a human-readable overview
- `EXAMPLE.md` — a worked example of the skill's input and output
- `metadata.json` — category, platform, and tagging metadata as used on creatorskills.co

## Install

### Claude Code

Copy the skill's folder into your project's `.claude/skills/` directory (or a personal `~/.claude/skills/` for every project):

```bash
curl -L https://github.com/calebvbi/creatorskills-free-skills/raw/main/skills/<skill-slug>/SKILL.md \
  -o .claude/skills/<skill-slug>/SKILL.md
```

Or clone the whole repo and copy the skills you want:

```bash
git clone https://github.com/calebvbi/creatorskills-free-skills.git
cp -r creatorskills-free-skills/skills/<skill-slug> .claude/skills/<skill-slug>
```

Claude Code picks up any `SKILL.md` under `.claude/skills/<name>/` automatically — no restart needed.

### Claude.ai / Claude Projects

Open a Project, go to **Project knowledge**, and upload the skill's `SKILL.md` as a file. Reference it by name in your prompt (e.g. "use the YouTube Chapter Generator skill on this transcript").

### Cursor

Cursor rules use a different frontmatter (`alwaysApply: true`) than the raw `SKILL.md` format. Create `.cursor/rules/<skill-slug>.mdc`, add `---\ndescription: <one-line summary>\nalwaysApply: true\n---` at the top, then paste in everything below the `SKILL.md`'s own frontmatter.

### Any other agent runtime

Every file here follows the open [Agent Skills](https://www.anthropic.com/news/skills) standard — plain markdown with YAML frontmatter (`name`, `description`, `metadata`). Any runtime that supports that standard can load these directly.

## License

MIT — see [LICENSE](LICENSE). Use, modify, and redistribute freely, including commercially, with attribution preserved per the license text.

## About CreatorSkills

[CreatorSkills](https://creatorskills.co) is a marketplace for AI skills built for content creators — YouTubers, podcasters, TikTokers, newsletter writers, and freelancers — covering Claude, ChatGPT, Cursor, and other platforms. The skills in this repo are the free tier; the full catalog (including multi-file skill packs and paid skills) is at [creatorskills.co](https://creatorskills.co).
