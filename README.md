# Subtitles Style
Ready-to-use ass subtitle styles ;)

## How-to
Put any "Style:" configuration under the "[V4+ Styles]" section, just below "Format:":

```
[V4+ Styles]
Format: Name, Fontname, Fontsize, PrimaryColour, SecondaryColour, OutlineColour, BackColour, Bold, Italic, Underline, StrikeOut, ScaleX, ScaleY, Spacing, Angle, BorderStyle, Outline, Shadow, Alignment, MarginL, MarginR, MarginV, Encoding
Style: Default,DejaVu Sans,16,&H0000FFFF,&H00FFFFFF,&H00000000,&H00000000,0,0,0,0,100,100,0,0,1,0.7,1.4,2,10,10,10,0
```

### Convert to .ass
Use `ffmpeg` to convert to `.ass` format, for example:

```bash
ffmpeg -i my_subs.vtt my_subs.ass
```

### Preview subtitles
Players like `mpv` or `vlc` automatically load subtitles with a video if subs have the same name, for example:

```
summer video.mp4
summer video.en.vtt
summer video.fr.ass
```

The output of `ffmpeg` can be previewed by using `ffplay`:

```bash
ffplay summer\ video.mp4 -vf subtitles="summer\ video.fr.ass"
```

### Burn subtitles
```bash
ffmpeg -i summer\ video.mp4 -vf subtitles="summer\ video.fr.ass" summer\ video.sub-fr.mp4
```

For more info: https://trac.ffmpeg.org/wiki/HowToBurnSubtitlesIntoVideo

## Styles
### Naming
```
1080p dejavusans 16 yellow raised
^     ^          ^  ^      ^
|     |          |  |      |
|     |          |  |      look
|     |          |  font color
|     |          font size
|     font name
resolution
```

### 1080p dejavusans 16 yellow raised
```
Style: Default,DejaVu Sans,16,&H0000FFFF,&H00FFFFFF,&H00000000,&H00000000,0,0,0,0,100,100,0,0,1,0.7,1.4,2,10,10,10,0
```

![](screenshots/1080p-dejavusans-16-yellow-raised.png)

