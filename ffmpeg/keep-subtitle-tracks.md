# Keep Subtitle Tracks when Transcoding

To keep all existent subtitle tracks when transcoding media with ffmpeg, just pass the flag `-map 0:s -c copy`, e.g.

```bash
$ ffmpeg -i /path/to/media.{mkv,mp4} -map 0:s -c copy
```

