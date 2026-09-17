# Viral Video Remake Skill

English | [简体中文](./README.zh-CN.md)

Break a short video that worked into its hook, beats, and call to action, then rebuild that structure around your own subject as a shot list, beat frames, and narration, delivered as one vertical clip or as segmented sources with captions and a timecoded edit list, from inside Claude Code, Codex, or OpenClaw.

> [!IMPORTANT]
> Rendering needs a [Beatra](https://beatra.ai) account and uses credits. The skill itself is free to install.

| Question | Answer |
| --- | --- |
| **What it does** | Paste the link or bring the file, break a short video that worked into its hook, beats, and call to action, then rebuild that structure around your own subject as a shot list, beat frames, and narration — delivered as one vertical clip animated from your opening frame, or, when the reference cuts too fast or runs too long for a single take, as segmented sources with captions and a timecoded edit list. |
| **Requirements** | Python 3.10+ and an agent that loads `SKILL.md` |
| **Cost** | Free to install. Each render uses credits on your Beatra account, and paid steps run only when you ask for that exact render or approve its card. |
| **Works with** | Claude Code, Codex, OpenClaw |

| Skill | Entry point | Version |
| --- | --- | --- |
| [`viral-video-teardown-remake`](skills/viral-video-teardown-remake) | [SKILL.md](skills/viral-video-teardown-remake/SKILL.md) | 0.3.0 |

This repository is published automatically from [beatra-ai/beatra-skills](https://github.com/beatra-ai/beatra-skills/tree/main/skills/viral-video-teardown-remake). Report issues there.

## Install

With the [`skills`](https://skills.sh) CLI:

```bash
npx skills add beatra-ai/viral-video-remake-skill
```

With the GitHub CLI:

```bash
gh skill install beatra-ai/viral-video-remake-skill viral-video-teardown-remake
```

Or clone this repository and copy `skills/viral-video-teardown-remake` into `~/.claude/skills/` for Claude Code,
`~/.agents/skills/` for Codex, or `~/.openclaw/skills/` for OpenClaw.

Or paste this into your agent:

```text
Install the viral-video-teardown-remake skill from https://github.com/beatra-ai/viral-video-remake-skill (folder skills/viral-video-teardown-remake), then follow its SKILL.md to connect my Beatra account.
```

## What you get

- **Read the structure, not just the surface** — Segment the clip into hook, body beats, and call to action with second-level timings, and name the script pattern underneath it.
- **Know what actually carried it** — Separate the structural move from the specific content and the presentation craft, so you carry over the part that transfers.
- **End with shootable material, not a report** — Get a shot list with visuals and narration kept apart, generated beat frames delivered as stills, a narration track, and — depending on how the reference cuts — either one vertical clip animated from your opening frame, or segmented sources with captions and a timecoded edit list for your own cut.

## Use cases

- **Study a competitor's breakout post** — Work out why a rival's short took off and build your own version on the same structure.
- **Turn a saved reference into a format** — Convert a clip from your swipe file into a repeatable shape you can run on new subjects.
- **Rebuild a benchmark under your brand** — Keep the pacing and beat order that proved itself, and replace every claim with your own.

## FAQ

### What do I need to start?

A reference short and a sentence about what your version is about. The reference can be a link to the post on TikTok, Douyin, Xiaohongshu, Instagram, YouTube, or X, a video file, screenshots of the key moments, a transcript, or your own description of what happens beat by beat.

### What does the teardown actually tell me?

A beat table with second-level timings, the script pattern the clip follows, a ranked read of what carried its performance, a score across hook strength, information density, pacing, subject presentation, emotional curve, and conversion pull, and the one weakness your remake can improve on.

### What do I get at the end?

A shot list where the on-screen action and the spoken line are written as separate fields, generated frames for the beats you choose, and a narration track in a voice you select. For a short, low-cut reference that fits inside one model take, that becomes one 9:16 vertical clip animated from your opening frame with the narration running over it, and the other beat frames come back as stills for your own edit. For a reference with more cuts, or one that runs longer than a single take supports, you instead get segment sources for every beat, that same single narration track, captions, and a timecoded edit list to assemble in your own editor.

## Updates

Each installed skill checks for a new version at most once a day, verifies the
official archive before replacing itself, and leaves your installation untouched
if anything fails. Turn it off at any time — see
`references/automatic-updates-and-safety.md` inside the skill.

## License

[MIT-0](LICENSE) — free to use, modify, and redistribute, including
commercially. No attribution required. Same terms as these skills carry on
ClawHub.
