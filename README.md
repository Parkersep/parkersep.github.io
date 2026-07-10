# parkersep.github.io

Personal portfolio site, published via GitHub Pages at https://parkersep.github.io
Unlisted: `noindex` meta + `robots.txt` keep it out of search engines; anyone with the link can view.

## Current media (in `assets/`)

| Slot | File | Source |
|---|---|---|
| Bimanual — main video | `vial-stack.mp4` | Custom OpenArm variant vial placement |
| Bimanual — thumbs | `yuri-render.jpg`, `yuri-photo.jpg` | Render + real photo |
| Foundation models — main | `g1-groot-pick-place.mp4` | GR00T N1.7 on Unitree G1 |
| Foundation models — thumb | `teleop-stacking.mp4` | Isaac Sim teleop, stock OpenArm |
| Landscaping — main | `go2w-blower.mp4` | Autonomous lawn blowing |
| Landscaping — thumbs | `mower.jpg`, `go2w-locomotion.mp4`, `edge-mowing.mp4` | Mower photo, sim locomotion, edge-mowing PoC |
| Mecanum | `mecanum-wiring.jpg` + `robot-wiring.pdf`, `controller-wiring.pdf` | Wiring diagrams |
| HFCWO | `hfcwo.jpg` + `hfcwo-presentation.pdf` | Final presentation |
| Flame diverter | *(placeholder — add `flame-diverter.jpg` and update index.html)* | |

Highlight reel is a YouTube embed (video ID `IEHpABjRHOE`) in `index.html`.

## Adding / replacing media

Videos: keep under ~25 MB, strip audio, 720p30 is plenty. Compress with:

```bash
ffmpeg -i input.mp4 -vf "scale=1280:-2,fps=30" -c:v libx264 -crf 27 -preset medium -an -movflags +faststart output.mp4
```

Poster frame for a video:

```bash
ffmpeg -ss 5 -i video.mp4 -vframes 1 -q:v 4 video-poster.jpg
```

Then reference the files in `index.html`, and:

```bash
git add -A && git commit -m "Update media" && git push
```
