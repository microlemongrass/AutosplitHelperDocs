---
title: Video
weight: 10
bookToc: false
---

# Video

{{<hint info>}}
Items related to video playback. The ```Seek``` column of the table is involved.
{{</hint>}}

{{< figure src="/image/ash/setvideo001.png" class="center" >}}

You can open up to two video windows at the same time.
- Normal video playback window (```Normal```)
- A window that seeks a video every split by referring to the value of the Seek column in the table (```Seek```)
  
　
### Pass 
Specify the video path. Supported videos are videos that can be played with Windows Media Player.

　
### Start at
Specify playback start position of video. Playback position when the first matching judgment occurs.

　
### Video size
Specify the video playback window size. (Maximum: 1920x1080)

　
### Start Speedrun manually
Check this if you can not start Speedrun automatically and do it manually. Wait until you press the key corresponding to Split after starting monitoring.

　
## About Seek Window
When playing a video in the Seek window, seek is performed at the time specified in the ```Seek``` column of the table when matching. Use this when you want to synchronize the current play and video for each split.

It is convenient to input time after creating a template, measuring the time using the recorded video as the source, and copying and pasting the obtained split time.

Since it is necessary to input "ss.ff" in ASH, if the format is different such as "mm:ss.ff", use [Tool]-> [Convert Seektime to "ss:ff"].

{{<hint info>}}
If you enter -1 in the ```Seek``` column, seek isn't performed.
{{</hint>}}

{{<hint warning>}}
Depending on the encoding format of the video, there may be a delay in the playback and seeking of the video. Seek more smoothly by reducing the encoding setting and changing the following settings.
```
keyint = {framerate}
```
{{</hint>}}