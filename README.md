# Elena Benzmüller — Sports CV

Static single-page site served via GitHub Pages at
<https://cbenzmueller.github.io/elena-benzmueller/>.

- `index.html` — the whole page (no build step, no dependencies)
- `img/` — photos, resized to ≤1600px and stripped of metadata (EXIF/GPS)
- `docs/` — saved copies of result pages that may not stay online (PDF)
- `media/` — short video clips (H.264 MP4, ≤720p) with poster frames

To add a photo: `sips -Z 1600 -s format jpeg -s formatOptions 80 in.jpg --out img/name.jpg`
(then `exiftool -all= img/name.jpg` if exiftool is installed, to drop EXIF/GPS).

To add a clip: `ffmpeg -i in.mov -vf scale=-2:720 -c:v libx264 -crf 24 -pix_fmt yuv420p -c:a aac -b:a 96k -movflags +faststart media/name.mp4`

Built in the same layout as the sibling site <https://cbenzmueller.github.io/max-benzmueller/>.
