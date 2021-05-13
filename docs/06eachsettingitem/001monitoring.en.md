---
title: Monitoring
weight: 1
bookToc: false
---

# Monitoring
{{<hint info>}}
There are some basic settings such as how to import game screens. 
{{</hint>}}

{{< figure src="/image/ash/setmonitoring001.png" class="center" >}}


### Capture method
Specify how to import the screen of games.
Virtual: Virtual camera such as "SCFF DSF"
Screen: Direct capture of the desktop screen
  
{{<hint warning>}}
For screen capture, if the capture size is large (1280x720 or more), the capture speed and similarity calculation speed will be significantly reduced, so it is recommended to use Virtual Capture (among them, OBS-VirtualCam).
{{</hint>}}

　
### ■Monitor fps
Specify the monitoring interval by framerate.

*In Windows 10 2004, there was Windows specification change related to this item. Explains the behavior when Windows is up to date.

#### For Screen Capture (Type: Window)
Over 60 \
→ It will be about 63fps regardless of the presence or absence of high accuracy check.
Since frame dropping always occurs, the actual accuracy will decrease.

60 or less \
→ When high accuracy check is on, fps will be the set value.
  When there is no high accuracy check, the monitoring interval is (1000 / 16n) fps. About 63/31/21/17 / ... fps


#### For Screen Capture (Type: WGC)
This is the refresh rate of the monitor. The setting value has no effect. The degree of frame dropping depends on the PC spec.


#### For Screen Capture (Type: Desktop)
fps is well below the set value. Please use Type: Window or WGC unless you have a specific reason.


#### For Virtual capture
Set the setting value according to the frame rate entered in the Virutal Capture settings. It seems that the degree of frame dropping depends on the PC specifications.\
The high accuracy check does not affect it, it only increases the CPU load, so uncheck it.

　
### Parallel processing
By parallelizing the similarity calculation process, it is possible to suppress the processing speed reduction when monitoring several templates at the same time.

A setting value of 3 to 4 is sufficient (it seems that it does not work. MaxDegreeOfParallelism is set.)

{{<hint danger>}}
Using Parallel processing can lead to instability. In that case, disable parallel processing.
{{</hint>}}

　
### Target of automation(Split/Loop/Reset/Load remover)
Specified monitoring target.\
When the loop is checked, the first image (second from the top in the table) is monitored the specified number of times.

{{<hint warning>}}
Even if you use a loop, you need to create two or more images for Split.
{{</hint>}}

　
### Default parameter (part)
For a description of each item itself, refer to [Table Description]. It is used when the default value when a new template image is created and when each item is applied to the table at once.

　
### Scenechange
It is used when the timing to operate the timer is set to 2 (after a scene change). Judgment occurs when the color specified in the target range (the range specified in PX(S) / PY(S) / SX(S) / SY(S) in the table) exceeds the specified threshold.

Color-Allowable range indicates the allowable range of color shift specified in the scene change. For example, if (R, G, B) = (100, 100, 100) and the allowable value is 10, then 90 <= R <= 110, 90 <= G <= 110, 90 <= B <= 110. It is considered to be that color.

