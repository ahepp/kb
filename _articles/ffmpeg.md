---
layout: default
---
## Examples

### Stream to twitch.tv

```
ffmpeg \
    -re -i "$FILE_PATH" \
    -vf subtitles="$FILE_PATH" \
    -c:v libx264 \
    -preset medium \
    -b:v 6000k \
    -maxrate 6000k \
    -bufsize 6000k \
    -pix_fmt yuv420p \
    -g 50 \
    -c:a aac \
    -b:a 160k \
    -ac 2 \
    -ar 44100 \
    -f flv rtmp://sea.contribute.live-video.net/app/$TWITCH_KEY
```
