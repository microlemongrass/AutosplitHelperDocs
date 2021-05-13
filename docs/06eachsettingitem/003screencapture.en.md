---
title: Screen Capture
weight: 3
bookToc: false
---

# Screen Capture

{{<hint info>}}
This item must be set if the capture method is set to ```Screen```.
{{</hint>}}

{{< figure src="/image/ash/setscreencapture001.png" class="center" >}}

### Capture type
Select from "window capture", "WindowsGraphicsCapture" or "desktop capture" (direct screen capture).

You can capture the specified window by selecting either type, selecting the window you want to capture from the list below, and pressing ```Initialize rect```.

　
#### Type:Window (Bitblt)
This is a so-called window capture.\
There are two ways to select it: select the window you want to capture from the list, or press ```Select``` to select the window you want to capture.\
After selecting the window by either method, press ```Initialize rect``` to make the entire window the capture range. Be sure to press it when specifying for the first time.

{{<hint info>}}
If you need to reselect the window, you can capture the same range as before by not pressing ```Initialize rect```.
{{</hint>}}
　
#### Type:WGC
Capture using Windows Graphics Capture. Usage is same as Type: Window.

{{<hint warning>}}
Only available on Windows 10 2004 or above.
{{</hint>}}
　
#### Type:Desktop
It is a desktop capture. Use this when window capture / Windows Graphics Capture is not available.\
The method of specifying the capture range is the same as for Type:Window (it may be better not to specify using ```Select```).

* By checking ```Follow```, the movement of the selected window will be detected and followed. Specify before adjusting the cropping.\
\
\
The resolution when actually performing processing such as monitoring on ASH can be specified in ```View resolution```. 

{{<hint info>}}
The smaller the size and display resolution of the window to be captured, the less CPU load. For example, when selecting capture software, you can reduce the CPU load by reducing the window size of the capture software in advance.
{{</hint>}}


{{<hint info>}}
Applications that cannot be captured by window capture, such as hardware acceleration enabled, can be captured by using Windows Graphics Capture or desktop capture.\
\
Windows Graphics Capture can capture almost any window, but it has a high CPU load.
{{</hint>}}

  Type         | Window   | WGC     | Desktop
---------------|----------|---------|---------
  App that can capture | Limited | Almost all| All  When a window is hidden by another window | Can capture | Can capture| Can't capture
  Framerate | Up to about 63fps | Monitor's refresh rate| Up to about 30fps
  Frame drop | Always occur | May occur (depends on specs?)| Always occur
  CPU load | Low | High| High

　
### Select
 Even if the application is disabled for hardware acceleration, it may not be captured normally (AmarecTV4 etc.). In that case, try to use ```Select```.

　
### Cropping
If there is a black band or other part you want to erase in the captured video, you can delete the corresponding part by specifying the crop range from ```Setting```.

{{< figure src="/image/ash/setscreencapture002.png" class="center" >}}


{{<hint info>}}
- For window capture, the coordinates at the top left of the window are (0, 0).
- For desktop capture, the upper left coordinate of the desktop is (0, 0).

- "16: xxx" in the cropping frame is the aspect ratio after cropping. You may get good results if you crop to match the aspect ratio of your game.
{{</hint>}}