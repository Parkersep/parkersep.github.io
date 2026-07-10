# parkersep.github.io

Personal portfolio site, published via GitHub Pages at https://parkersep.github.io

## Adding videos and images

Drop files into `assets/` with these exact names — the site picks them up automatically
(video preferred, image used as fallback if no video exists):

| Project | Video | Image fallback |
|---|---|---|
| Bimanual Manipulation Platform | `assets/bimanual.mp4` | `assets/bimanual.jpg` |
| Autonomous Landscaping Robots | `assets/quadruped.mp4` | `assets/quadruped.jpg` |
| Mecanum Robot | `assets/mecanum.mp4` | `assets/mecanum.jpg` |
| Flame Diverter | `assets/flame-diverter.mp4` | `assets/flame-diverter.jpg` |
| HFCWO Device | `assets/hfcwo.mp4` | `assets/hfcwo.jpg` |

Then commit and push:

```bash
git add assets/ && git commit -m "Add project media" && git push
```

**Video guidelines:** keep each mp4 under ~25 MB (GitHub hard-limits files at 100 MB and
the repo stays fast to load). 30–60 seconds, 1080p, H.264. To compress:

```bash
ffmpeg -i input.mp4 -vcodec libx264 -crf 28 -preset slow -an -vf scale=1280:-2 output.mp4
```

## Before adding work footage

Get Sensori's OK before publishing videos/photos of the bimanual platform or the
landscaping robots — they're unreleased products tied to a pending licensing deal.
Personal projects (mecanum, flame diverter, capstone) need no permission.
