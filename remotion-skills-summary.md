# Remotion Skills: Summary (updated)

This is the current state of the Remotion skills installed for this project. Each entry is based on the `SKILL.md` and reference or rule files from a clone of the source repo. Skill scripts and `install.sh` files were not run.

Installed skills live in `~/.agents/skills/` (symlinked for Claude Code and other agents). `skills-lock.json` in this repo records each skill's source.

---

## Changes since the last summary

- **Removed:** `digitalsamba/claude-code-video-toolkit` (`remotion`) and `liamrjohnston/remotion-motion-graphics-skill` (`motion-graphics`).
- **Installed:** `calesthio/openmontage` (`remotion`). This resolves the `remotion` name collision.
- **Still open:** The `remotion-best-practices` collision. The remotion-dev official version was replaced by the json-render version. The json-render `remotion` renderer skill is not installed.
- **Lock file:** `skills-lock.json` was updated by hand to drop `motion-graphics`. The `skills remove` command did not update it.

---

## Installed skills (16)

| Skill | Source | Purpose |
|---|---|---|
| `remotion` | calesthio/openmontage | Shared components, custom transitions, and project conventions |
| `remotion-best-practices` | vercel-labs/json-render | Router to 34 topic-specific rule files |
| `create-remotion-geist` | vercel-labs/skill-remotion-geist | Vercel Geist style guide |
| `remotion-video` | iart-ai/motion-design-skills | Programmatic video guide with still-frame verification |
| `remotion-video-toolkit` | sheshiyer/skill-clusters | About 29 rules covering the full feature set |
| `remotion-captions`, `-create`, `-docs`, `-interactivity`, `-maps`, `-markup`, `-multimedia`, `-render`, `-saas`, `-studio`, `-upgrade` | remotion-dev/skills | Official Remotion skills, one per area |

---

## Skill-by-skill summary

### 1. calesthio/openmontage, `remotion` (new)
- **What it is:** A "toolkit extensions" skill from the OpenMontage AI video production project. OpenMontage has 88 skills in total. Only this one was installed.
- **Covers:**
  - Seven custom transitions with options: `glitch`, `rgbSplit`, `zoomBlur`, `lightLeak`, `clockWipe`, `pixelate`, `checkerboard`.
  - Duration guidelines per transition type (15 to 60 frames).
  - Shared components: `AnimatedBackground`, `SlideTransition`, `Label`, `Vignette`, `LogoWatermark`, `SplitScreen`, `NarratorPiP`, `Envelope`, `PointingHand`, `MazeDecoration`.
  - Timing conventions: title 3 to 5 s, overview 10 to 20 s, stats 8 to 12 s, credits 5 to 10 s, and about 150 words per minute for voiceover.
  - Eight best practices: frame-based animation only, `fps` from `useVideoConfig()`, clamped interpolation, `OffthreadVideo`, `delayRender` for async data, `staticFile` for assets, 30 fps, and constant `playbackRate`.
- **Caveat:** The transitions and components live in a `lib/` folder that is not part of the skill, so they will not work on their own. The skill also points to a `showcase/` folder for previews.

### 2. vercel-labs/json-render, `remotion-best-practices`
- **What it is:** A router skill with 34 rule files that Claude loads when working with Remotion code.
- **Topics:** 3D (Three.js / R3F), animations, assets, audio, calculate-metadata, captions, charts, compositions, fonts, GIFs, images, light leaks, Lottie, DOM and text measurement, sequencing, Tailwind, text animations, timing and interpolation, transitions, transparent videos, trimming, videos, parametric props with Zod, Mapbox maps, and Mediabunny utilities.
- **Best for:** General-purpose Remotion reference. The most comprehensive "look it up" skill installed.
- **Caveat:** This version replaced the remotion-dev one.

### 3. vercel-labs/skill-remotion-geist, `create-remotion-geist`
- **What it is:** A style guide for videos that match Vercel's Geist design system.
- **Look and feel:** Dark theme (`#0a0a0a` background), Geist typography from jsDelivr, the 10-step Geist color scale, and a 4px spacing base.
- **Motion:** Spring animations (`damping: 200`) with fade-in and spring-scale helpers.
- **Rules:** No emojis (use `@geist-ui/icons`), use official brand assets rather than hand-drawn SVGs, and use `prism-react-renderer` for code blocks.
- **Includes:** Reference files for setup, icons, code blocks, colors, typography, components, scene patterns, and storyboards.
- **Best for:** Polished, on-brand product and launch videos.

### 4. iart-ai/motion-design-skills, `remotion-video`
- **What it is:** A programmatic video guide (version 0.1.0) covering React compositions rendered via CLI or `@remotion/renderer`.
- **Core techniques:** Frame-driven animation with `useCurrentFrame`, clamped `interpolate`, and `spring`. Scheduling with `<Sequence>` and `<Series>`, including negative offsets for crossfades. Zod `schema` and `defaultProps` for parametric props. Beat sync from timestamps detected offline.
- **Verification workflow:** Render still frames at the start, middle, and end, and inspect them before encoding the full MP4.
- **Gotchas:** No `Math.random()`, `Date.now()`, or timers (use `random(seed)`). Load fonts with `staticFile` and `delayRender`.
- **Caveat:** It refers to `scripts/contact-sheet.sh` and `scripts/probe-mp4.sh`, which are not in the source repo.

### 5. sheshiyer/skill-clusters, `remotion-video-toolkit`
- **What it is:** A rule-based toolkit with about 29 rules in a `rules/` folder.
- **Covers:** Compositions, rendering (CLI, Node.js, AWS Lambda, Cloud Run, Express), animation and timing, sequencing, transitions, trimming, text effects, fonts, media embedding, captions (Whisper, Deepgram, AssemblyAI; TikTok-style highlighting; SRT import), animated charts, 3D, Lottie, Tailwind, and media utilities.
- **Also includes:** Use-case ideas and a render-as-a-service pattern.
- **Requirements:** Node 18+, React 18+, and `npx create-video@latest` for scaffolding.
- **Caveat:** Its "Contribute" link points to a different GitHub repo (`shreefentsar/remotion-video-toolkit`) than the one it was installed from.

### 6. remotion-dev/skills (official), 11 skills
- `remotion-captions`, `-create`, `-docs`, `-interactivity`, `-maps`, `-markup`, `-multimedia`, `-render`, `-saas`, `-studio`, `-upgrade`.
- These cover the official Remotion docs by area. `remotion-best-practices` from this set is no longer installed.

---

## Removed skills

- **`digitalsamba/claude-code-video-toolkit` (`remotion`):** Removed. Its shared components and transitions overlap with the openmontage skill. It also referred to a `remotion-official` skill that was never installed under that name.
- **`liamrjohnston/remotion-motion-graphics-skill` (`motion-graphics`):** Removed. It is a gated workflow for short promo clips that required a Node gate script and the `cinematic-camera` skill (which was never installed). Reinstall it if you want that strict workflow later.

---

## Overlap and conflicts

- **Video components:** Some skills recommend `<OffthreadVideo>` and `<Audio>` from `remotion`. Others point to `<Video>` and `<Audio>` from `@remotion/media`.
- **Transitions:** The openmontage and iart skills both touch transitions and sequencing. The official `@remotion/transitions` package is also referenced.
- **Core rules:** All of them agree on frame-driven animation, clamped interpolation, and `delayRender` for async work.

---

## Open items

1. Decide what to do about `remotion-best-practices`. Options: keep the json-render version, or reinstall the remotion-dev version under a different name.
2. Review skill code before relying on it. Skills run with full agent permissions. Only the `SKILL.md` files and their reference lists have been read.
