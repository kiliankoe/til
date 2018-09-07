# Choose a Specific Format to Download

List all formats using `-F`.

```
$ youtube-dl -F http://www.youtube.com/watch?v=HRIF4_WzU1w
[youtube] Setting language
[youtube] HRIF4_WzU1w: Downloading webpage
[youtube] HRIF4_WzU1w: Downloading video info webpage
[youtube] HRIF4_WzU1w: Extracting video information
[info] Available formats for HRIF4_WzU1w:
format code extension resolution  note 
171         webm      audio only  DASH webm audio , audio@ 48k (worst)
140         m4a       audio only  DASH audio , audio@128k
160         mp4       192p        DASH video 
133         mp4       240p        DASH video 
134         mp4       360p        DASH video 
135         mp4       480p        DASH video 
17          3gp       176x144     
36          3gp       320x240     
5           flv       400x240     
43          webm      640x360     
18          mp4       640x360     (best)
```



Choose a specific format to download using the format code.

```
$ youtube-dl -f 140 <url>
```
