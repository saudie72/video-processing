# Video Processing: OpenCV video challenges

My work for the computer vision course's video module (Lab 4 / Lecture 5), in one notebook: **`SF_video_player_challenge.ipynb`**.

| Challenge | What it does | Output |
| --- | --- | --- |
| 1. Video player | Plays a video at its true speed (from its FPS); **p** pauses/resumes, **q / Q / Esc** quits | OpenCV window |
| 2. Grayscale, half speed | Grayscale race car at half speed, banner `Frame: n` starting at `Frame: 1` | `race_car_gray.avi` |
| 3. My own video | `falls_1080p.mp4` (downloads from this repo) stamped with my name and a timestamp on every frame, written slow (0.5x), normal and fast (2x), then played in the notebook and in an OpenCV window | `falls_slow.mp4`, `falls_normal.mp4`, `falls_fast.mp4` (+ `_h264` copies) |

## Run it

```bash
pip install -r requirements.txt
jupyter notebook SF_video_player_challenge.ipynb   # or open it in VS Code
```

Run on your own computer: Challenges 1 and 3.6 open desktop windows (`cv2.imshow`), which Google Colab cannot show. The race car clips download automatically from the course repo ([fenago/cv2](https://github.com/fenago/cv2), Mod4).

## Notes

- `falls_1080p.mp4` is a 1080p H.264 copy of my 4K original (190 MB, over GitHub's 100 MB file limit).
- Slow and fast are the same 900 frames written with a different FPS number: 15, 30 and 60 FPS play for 60, 30 and 15 seconds. The timestamp shows source time, so all three end at 00:30.00.
- OpenCV writes `mp4v`, which browsers cannot play, so the notebook re-encodes to H.264 with ffmpeg (from `imageio-ffmpeg` if ffmpeg is not installed) before showing videos inline.
