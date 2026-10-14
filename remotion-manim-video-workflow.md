# Step-by-step workflow: math video with Manim + Remotion

This workflow makes a 9:16 (1080×1920, FHD) explainer video. Manim draws the mathematics. Remotion assembles the final video with narration, captions, branding, and a sources card. It follows the conventions of the PM-manin-math repo (`https://github.com/prasad-kmd/PM-manin-math`) and uses the three installed skills:

- `manim-explainer-animation` (calesthio/generative-media-skills): production workflow, QA, and render settings.
- `manim-composer` (adithya-s-k/manim_skill): research, questions, and `scenes.md` planning.
- `clarity` (addyosmani/clarity): narration and longer prose.

Work through the steps in order. Each step lists its output, so you can check progress before moving on.

---

## Step 0. Fix the brief (5 min)

Write these down before anything else. Put them at the top of `research/<topic>/brief.md`.

| Item | Default from PM-manin-math | Your value |
|---|---|---|
| Topic | — | |
| Length | 75–90 s (Shorts-style) | |
| Audience | general / undergraduate | |
| Visual style | Classic 3Blue1Brown (suggest alternatives after research) | |
| Aspect ratio | 9:16, FHD 1080×1920 | |
| Frame rate | 60 fps (final), 15 fps (quick tests) | |
| Branding | `@prasadkmd` watermark, small, plus YouTube icon | |
| Sources | Shown on a silent final card, short form | |

Also write the learning objective in one sentence and the core misconception or paradox in one sentence. The `manim-explainer-animation` skill asks for both.

**Output:** `research/<topic>/brief.md`

---

## Step 1. One-time setup

Do this once per machine or container.

### 1a. Install the agent skills

```bash
npx skills add https://github.com/calesthio/generative-media-skills --skill manim-explainer-animation -y -a '*' < /dev/null
npx skills add https://github.com/adithya-s-k/manim_skill --skill manim-composer -y -a '*' < /dev/null
npx skills add addyosmani/clarity -y -a '*' < /dev/null
```

Read the installed `SKILL.md` for each before you start. Skill scanners reported "Med Risk" for `manim-composer` (Snyk). Review its scripts and templates before running anything from it.

### 1b. Clone the PM-manin-math repo

```bash
git clone https://github.com/prasad-kmd/PM-manin-math
cd PM-manin-math
```

Read these in order:

1. `README.md`: layout and the rule order for the docs.
2. `docs/design-system.md`, then `docs/visual-theme.md`, `docs/layout-guidelines.md`, `docs/typography.md`, `docs/animation-style.md`, `docs/mathematical-visualization.md`, `docs/branding.md`, `docs/scene-structure.md`.
3. `docs/agent-workflow.md`: the before-writing, while-writing, and before-finalizing checks.

`docs/additional/` may conflict with the main docs. Use it for ideas only.

### 1c. Install Manim and its system dependencies

Follow `instructions-manim.md` in the repo. The short version:

```bash
sudo apt-get update && sudo apt-get install -y ffmpeg
sudo apt-get install -y texlive-latex-base texlive-fonts-recommended texlive-latex-recommended dvisvgm
pip install manim==0.22.0     # check the version pin in the repo before installing
manim checkhealth             # expect 4 PASSED: manim, executable, latex, dvisvgm
```

If the LaTeX install fails with a hash mismatch, run `sudo apt-get update` and retry with `--fix-missing`.

### 1d. Set up Remotion

```bash
npx create-video@latest remotion-studio   # choose a blank or TypeScript template
cd remotion-studio && npm install
```

Check the current Remotion docs for the scaffold command. Use the installed `remotion-best-practices` skill for rules on assets, video, audio, and rendering.

**Output:** `manim checkhealth` passes. The Remotion studio starts.

---

## Step 2. Research the topic

Use the `manim-composer` skill's Phase 1. Search the web for the core idea, the "aha" moment, and the common misconceptions. Keep the sources.

Write `research/<topic>.md` (the repo's `research/pi4-staircase-research.md` is a good model):

- The core facts, with their sources.
- The "aha" moment and the misconception to address.
- The sources, short form, for the end card (for example: `Source: Wikipedia – Taxicab geometry`).

Only use facts you have checked. Do not claim a result is in the repo unless you have opened the file.

**Output:** `research/<topic>.md` with a source list.

---

## Step 3. Plan the storyboard

Use `manim-composer`'s Phase 2 questions, then write `research/<topic>/scenes.md` from its template (`templates/scenes-template.md`). For each scene, record:

- Visual elements, the on-screen math, and the color assignments.
- The narration notes.
- Technical notes: which Manim objects and animations to use.

Split the story into **beats**. A beat is one idea that gets one narration line and one visual. Write them as data:

`research/<topic>/beats.json`

```json
[
  {"name": "hook", "dur": 4.2, "audio": "audio/01_hook.wav", "audio_dur": 3.2},
  {"name": "setup", "dur": 7.0, "audio": "audio/02_setup.wav", "audio_dur": 5.5}
]
```

`dur` is the time you give the beat on screen. `audio_dur` is the measured length of its narration. Keep `dur` a little longer than `audio_dur`.

**Output:** `scenes.md` and `beats.json`.

---

## Step 4. Write the narration with clarity

Narration is the one part where the writing needs care. Use the `clarity` skill in co-write mode, and give it the beat's content and the audience. Ask it to keep the claims in your research file.

Write one line per beat. Keep lines short enough to say in the beat's time. As a rough guide, a 60-second video is about 150 spoken words.

Write `research/<topic>/narration.json`:

```json
[
  {"name": "hook", "text": "Can π really equal four? Let's find out."},
  {"name": "setup", "text": "Start with a circle of diameter one, wrapped in a square."}
]
```

Review the text against `scenes.md` before generating audio. The skill's review and lint modes check for generic or padded prose.

**Output:** `narration.json`.

---

## Step 5. Generate voiceover audio

Pick a voice with `add_voice` (you choose from two auditions). Then generate one WAV file per beat with `generate_speech`, using the `text` from `narration.json`:

- File names match `beats.json`: `research/<topic>/audio/01_hook.wav`, and so on.
- Keep each call to 1500 characters or less.
- Measure each file's length (`ffprobe -v error -show_entries format=duration -of csv=p=0 file.wav`) and write it into `audio_dur` in `beats.json`.

**Output:** `research/<topic>/audio/*.wav` and an updated `beats.json`.

---

## Step 6. Build the timeline

Compute when each beat starts in the final video. Put the result in `research/<topic>/timeline.json`:

```json
{"beats": [
  {"beat": "hook", "start": 0.0, "dur": 4.2, "end": 4.2},
  {"beat": "setup", "start": 4.2, "dur": 7.0, "end": 11.2}
]}
```

Each `start` is the sum of the earlier beats' `dur`. The Manim scene must follow this timeline, so the visuals land on the narration. This is the same timeline the repo's `build_pi4_staircase.py` uses to position the audio.

**Output:** `timeline.json`.

---

## Step 7. Write the Manim scene

Create `scripts/<topic>.py` that follows the repo's conventions. Key points:

- **Reuse the repo's helpers and palette.** Look at `scripts/_theme.py` and `scripts/_layout.py` first. Do not define a second palette. Set the background to pure black (`#000000`) as the design system says.
- **Use the 9:16 frame.** Set the resolution in the scene config, and use the layout helpers. Do not assume a 16:9 composition will fit.
- **One Scene class per beat is easiest to test.** Build the full video from the beats, in order.
- **Match each beat's duration.** Use `self.wait()` and `run_time` so the beat's total length equals its `dur` in `timeline.json`.
- **Stable semantic colors.** Give the same variable or object the same color throughout.
- **Label moving objects.** Keep labels attached to what they describe.
- **Check the Manim API.** Confirm method names against the installed Manim version. Do not rely on memory.

Use `manim-composer`'s `references/` files for animation and visual techniques. Use `manim-explainer-animation`'s section on the graph, algorithm, and voiceover timing patterns.

**Output:** `scripts/<topic>.py`.

---

## Step 8. Preview, then render

Iterate with fast renders first:

```bash
# quick checks: low quality, one scene, a few seconds
manim -pql scripts/<topic>.py <SceneName>

# review the layout and timing at medium quality
manim -pqm scripts/<topic>.py <SceneName>

# still frames to check legibility and overlaps
manim -s scripts/<topic>.py <SceneName>
```

Use `manim -qk` (4K) only if the repo asks for it. The final render is `-qh` (1080p) at the target frame rate, or the repo's configured quality. Check the output folder name Manim actually creates. The repo's `build_pi4_staircase.py` expects `videos/<topic>/1920p60/<Scene>.mp4`. Make the path match what Manim writes, or update the build script.

Manim writes the silent video with no audio. Keep it that way for now. Remotion adds the audio in step 9.

**Output:** a silent Manim render, for example `videos/<topic>/<quality>/<Scene>.mp4`.

---

## Step 9. Assemble in Remotion

Put the Manim output in `remotion-studio/public/`. Then build one Remotion composition:

```tsx
import {AbsoluteFill, Audio, OffthreadVideo, Sequence, staticFile} from 'remotion';

// frames = seconds × fps. Use the timeline from step 6.
export const MathVideo: React.FC = () => (
  <AbsoluteFill style={{background: '#000'}}>
    <OffthreadVideo src={staticFile('<Scene>.mp4')} />
    {/* one <Audio> per beat, placed at its start time from timeline.json */}
    <Sequence from={Math.round(4.2 * 60)}>
      <Audio src={staticFile('audio/02_setup.wav')} />
    </Sequence>
    {/* watermark, lower-third, captions, and the sources card go here */}
  </AbsoluteFill>
);
```

Notes:

- **Video component.** The current Remotion docs recommend `<Video>` from `@remotion/media`. `<OffthreadVideo>` from `remotion` is still supported. Use whichever matches your installed version.
- **Audio.** Use one `<Audio>` per beat inside a `<Sequence>`, starting at the beat's `start` time. Keep the lead-in of about 0.3 s that the repo's build script uses.
- **Captions.** Generate `captions.srt` from `narration.json` and `timeline.json`, using the same format as `build_pi4_staircase.py`. Show captions in Remotion with `@remotion/captions`, or burn them in only if the platform needs open captions.
- **Watermark.** A small `@prasadkmd` label in a safe area, with the YouTube icon if you can get one. Check `docs/branding.md`.
- **Sources card.** Add a separate final frame, after the narration ends, that lists the sources in short form. Show it silently. Do not narrate it.
- **Composition.** `width={1080} height={1920} fps={60}`.

**Output:** the Remotion composition in `remotion-studio/src/`.

---

## Step 10. Render the final video

```bash
cd remotion-studio
npx remotion render MathVideo ../videos/<topic>/<topic>_final_1080x1920.mp4
```

Write the captions next to it as `videos/<topic>/<topic>_captions.srt`.

If you prefer to keep Remotion for visuals only, use the repo's ffmpeg path: `build_<topic>.py` muxes the audio and writes the SRT. The Manim video and the audio are the same in both paths.

**Output:** `videos/<topic>/<topic>_final_1080x1920.mp4` and the `.srt` file.

---

## Step 11. QA before you publish

Work through the layers in `manim-explainer-animation`'s QA section, then the checks in `docs/agent-workflow.md`:

1. **Code:** imports cleanly, scene names are correct, no hardcoded absolute paths.
2. **Render:** no clipped labels, overlapping text, missing glyphs, or stutter. Check the final file, not only the Manim output.
3. **Timing:** each beat's visual matches its narration. The viewer has time to read.
4. **Math:** formulas, units, and graph scales are correct. Check them against the sources.
5. **Accessibility:** captions match the narration. Text is readable on a phone. Contrast is high.
6. **Delivery:** the file is 1080×1920, the audio is in sync, and the length is within the target. Confirm with `ffprobe`.
7. **Provenance:** the sources card is present and correct. Sources and generated assets are logged.

Report what you tested. If you did not view the frames or watch the video, say so.

---

## Step 12. Publish package

Write `videos/<topic>/publish.md` with:

- Three title options.
- A description that includes the sources in short form.
- Hashtags.

The repo's research files show the format.

---

## Step 13. Keep it reproducible

- Commit `scripts/`, `research/`, `narration.json`, `beats.json`, `timeline.json`, `scenes.md`, the Remotion source, and `captions.srt`.
- Do not commit rendered video or media caches. The repo's `.gitignore` already covers `media/`. Check that it covers `*.mp4` as well.
- Record the Manim version, Remotion version, and TTS voice ID in the research folder.

---

## Quick reference

| Stage | Tool or skill | Output |
|---|---|---|
| Brief | your notes | `brief.md` |
| Setup | `npx skills`, `manim checkhealth` | working environment |
| Research | `manim-composer` Phase 1 | `research/<topic>.md` |
| Storyboard | `manim-composer` templates | `scenes.md`, `beats.json` |
| Narration | `clarity` | `narration.json` |
| Voice | `add_voice`, `generate_speech` | `audio/*.wav` |
| Timeline | your timing | `timeline.json` |
| Animation | Manim + repo helpers | `scripts/<topic>.py`, silent MP4 |
| Assembly | Remotion | final composition |
| QA | `manim-explainer-animation` QA | checked render |
| Publish | repo research format | `publish.md`, SRT |
