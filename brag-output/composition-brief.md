# HyperFrames Composition Brief: PhotoTrace

## Objective
Create a 20-second local-only launch video for PhotoTrace from the current Windows app code and README.

## Output
- Composition directory: `brag-output/composition/`
- Rendered video: `brag-output/brag.mp4`
- Format: landscape, 1920x1080, 30 fps
- Duration: 20 seconds

## Source material
- Project root: `C:\Users\chris\OneDrive\Documents\VsCode\GPX-Photo-Geotagger`
- Read: `README.md`, `src/geotagger/ui/main_window.py`, `src/geotagger/ui/theme.py`
- Product: PhotoTrace
- Actual labels to show: "Guided", "Preview matches", "Map Preview", "Create geotagged copies", "Outings"
- Promise: geotagged copies are made without changing source photos.
- Recreate a plausible workspace using fictional demo route and filenames. It is a UI reconstruction, not a recorded session.

## Creative direction
- Tone: polished, quiet field-tool film.
- Hook: "Your photos have a place."
- Outro: "Follow the route. Keep the originals."
- Keep all claims within the current README and code.

## Visual identity
- Background #f3f7f5, surface #ffffff, text #18352b, accent #176b4d, highlight #dff1e8.
- Segoe UI, from the Qt stylesheet.
- Real icon from `packaging/phototrace.png`.

## Storyboard
See `brag-plan.md`. Scenes: route hook 4.5s; Guided inputs 5s; Map Preview 5.5s; copies and brand 5s.

## Audio and local-only constraints
- No voice, avatars, hosted generation, paid API, publishing, or cloud render.
- Disable HyperFrames telemetry with `HYPERFRAMES_NO_TELEMETRY=1` and `DO_NOT_TRACK=1` on every CLI run.
- Use the locally installed HyperFrames CLI and FFmpeg only.
- Generate a small original synth bed and soft clicks with local FFmpeg; no third party music.
- Keep all runtime assets local, including GSAP.

## Validation
Run `hyperframes check`, inspect representative snapshots, render locally to MP4, extract a settled poster, bake it as frame zero, and verify duration and dimensions with FFprobe.
