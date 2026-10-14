# Can this Remotion setup be used with Manim for mathematical motion?

**Short answer: yes.** Manim makes the math animations, and Remotion places them into the final video. Manim does not need to run inside Remotion. The two tools hand off through a video file, and a transparent WebM keeps the background clear so the Remotion scene shows through.

## Recommended pipeline

1. **Write the math scene in Manim Community (ManimCE)** as a Python `Scene` subclass.
2. **Render it with a transparent background** in WebM format:

   ```bash
   manim -t --format=webm -qh scene.py MyScene
   ```

   - `-t` (`--transparent`) renders with an alpha channel. Manim's FAQ says this produces a `.mov` by default, because the default MP4 format cannot store transparency.
   - `--format=webm` selects WebM, which can carry alpha. The Manim docs say transparent MP4 is rejected.
   - `-qh` is high quality (1080p). Use `-ql` for quick previews. `-qm` is in between.
   - Manim's CLI reference lists the same flags, and the local `manimce-best-practices` skill documents `-t` and `--format webm`.

3. **Copy the WebM into the Remotion project**, usually under `public/`.
4. **Embed it in a composition** and use `staticFile()` to load it:

   ```tsx
   import { AbsoluteFill, staticFile, Sequence } from "remotion";
   import { Video } from "@remotion/media";

   export const MathScene: React.FC = () => (
     <AbsoluteFill style={{ background: "#0b1020" }}>
       <Sequence from={0} durationInFrames={240}>
         <Video src={staticFile("manim/scene.webm")} />
       </Sequence>
     </AbsoluteFill>
   );
   ```

   Current Remotion docs recommend `<Video>` from `@remotion/media`. `<OffthreadVideo>` from `remotion` is still supported and is shown in older examples. The local `remotion-best-practices` rules still use `<OffthreadVideo>`, so check which one matches your installed Remotion version.

5. **Render the final video** with `npx remotion render`. Remotion composites the WebM over the background.

## Transparency on the Remotion side

- If the final output is also a transparent overlay, the local transparent-video rule gives this command for WebM output: `npx remotion render --image-format=png --pixel-format=yuva420p --codec=vp9 MyComp out.webm`.
- If the final output is a normal opaque video, the Manim WebM does not need transparency. Rendering Manim with a solid background (no `-t`) is simpler.

## Mathematical text (LaTeX)

- **Manim** handles LaTeX itself. `MathTex` and `Tex` need a LaTeX install on the machine that renders Manim.
- **Remotion** has no built-in LaTeX rendering, as far as the docs I checked show. The clean approach is to keep equations inside Manim, so Remotion only plays the rendered video.
- If you want equations drawn live inside React instead, a math library like KaTeX or MathJax works. This is my suggestion and was not verified in the sources above.

## Things to check before building

- **Install Manim Community** (`pip install manim`) and a LaTeX distribution, then confirm `manim --version` and a test render.
- **Check the Manim version.** The docs I read were for v0.21 and v0.22.
- **Do not assume the Remotion-side component.** Check the Remotion version in your project: `@remotion/media` `<Video>` is the current recommendation.
- **Test alpha in your player.** WebM alpha is reliable in browsers and in Remotion. Check that your editor handles it if you open the file there.

## Sources

- Manim Community FAQ, transparent backgrounds (`-t`, `--format=webm`): https://docs.manim.community/en/stable/faq/general.html
- Manim Community output settings (`--format` values, transparent MP4 rejected): https://docs.manim.community/en/stable/tutorials/output_and_config.html
- Remotion asset docs (`<Video>` from `@remotion/media` recommended; `<OffthreadVideo>` listed as legacy): https://www.remotion.dev/docs/assets
- Local skill rules: `manimce-best-practices` (CLI section) and `remotion-best-practices` (`transparent-videos.md`), both in the installed skill sources.
