# Create a Video from an Image and Audio File

Technically something simple along the following lines would work. 

```sh
ffmpeg -i image.png -i audio.mp3 video.mp4
```

This does however create a file with just a single frame, which doesn't really work on YouTube for example. The following creates a video with repeating frames.

```sh
ffmpeg -r 1 -loop 1 -i image.png -i audio.mp3 -acodec copy -shortest -vf scale=1280:720 video.mp4
```

[Source](https://superuser.com/a/1041820/236423)
