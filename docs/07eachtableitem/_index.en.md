---
weight: 70
bookFlatSection: true
title: "Table description [Split/Reset]"
---

　
{{< figure src="/image/ash/table003.png" class="center" >}}
{{< figure src="/image/ash/table004.png" class="center" >}}
{{< figure src="/image/ash/table005.png" class="center" >}}

### Comment
Comment.
　
### No
Specify how many templates are monitored simultaneously in each segment.


#### 例
[0,1,2,3,4,5,6,...]\
→There is only one target for all segments (default).

[0,1,2,2,2,3,4,...]\
→In Segment 2 , there are 3 targets (2.png, 3.png, 4.png).


{{<hint warning>}}
The maximum number of images that can be monitored simultaneously is 300, but the limit is about 10 except for ```L2 Norm.```)
{{</hint>}}

　
### And
(When monitoring multiple templates at the same time) Specify the and condition and or condition.\
0 -> or\
1 -> and\
　\
Please note the following points when using ```or``` condition and ```and``` condition together.
- Matching processing is performed in order from the top of the table.\
-> Please set in the order of ```and``` condition -> ```or``` condition.

- Additional monitoring such as blackout standby is performed for templates that meet the following conditions.\
  　\
　(a) In case of only ```and``` condition -> Last template\
　(b) In case of only ```or``` condition  -> First template\
　(c)  When both ```and``` condition and ```or``` condition are used together -> First template of ```or``` condition


　
### Met. (Method)
Specify the image comparison method.

1. Template matching
2. RGB diff. (per pixel)\
 -Determine the color difference for each pixel and check how many pixels have a small color difference.
3. RGB diff. (sum)\
 -The sum of the color differences of each pixel.
4. RGB Specific color (%)
 -Check how much of the specified color is within the monitoring range.
5. RGB Specific color (pixel)\
 -Check how many pixels the specified color exists in the monitoring range.
6. Histogram
7. dHash
8.  L2 Norm
9. AKAZE


　
### Key
Specify which signal to send.
\
 -1 -> Not send\
 0 -> Split\
 1 -> Pause\
 2 -> Resume\
 3 -> Undo\
 4 -> Skip

　
### M(mask)
Specify whether to use a mask image.\
When using, please clear the part you want to exclude in the corresponding ```n.png```. 

Please refer to [here]({{< ref "/docs/10tips/009maskimage.en.md" >}}) for creating a mask image.

{{<hint warning>}}
Mask images cannot be used with ```dHash``` and ```AKAZE```.
{{</hint>}}

　
### A(Use Audio)
Specify whether to monitor using an audio device

0. Video
1. Audio

　　
### Thr.(Threshold)[0-100(%), 0.01 unit]
Specify the image matching threshold. The higher the value, the more severe the judgment.\
If the similarity is greater than or equal to this value, it is judged as a match.

{{<hint warning>}}
There are monitoring methods where the threshold does not fall within the range of 0 to 100% (```Template matching (with mask)```, ```RGB Specific color (pixel)```, ```AKAZE```). When using these, set the value referring to the actual similarity calculation result.
{{</hint>}}

　
### PN(Positive/Negative)
In normal monitoring, the threshold is treated as follows.
- p -> Positive matching (whether it exceeds the threshold)
- n -> Negative matching (whether it is below the threshold)

*Please enter in lowercase letters.

　
### Sleep[0-(s), 0.1 unit]
Waiting time from image matching to the start of the next monitoring.

{{<hint info>}}
If the next image recognition is set to be long enough not to hinder the image recognition, the risk of false recognition will be reduced.
{{</hint>}}

　
### T(Timing)
Specify the timing of hot key emulation.


0. Send immediately 
1. Send after waiting "Delay"
2. The range specified by ```PX(S)/PY(S)/SX(S)/SY(S)``` is changing to specific color (Please see Parameter setting's "Scene change") + after waiting "Delay" 
3. After matching, the similarity is smaller than the threshold value in the monitoring method used at the time of matching + after waiting "Delay"

　
### Delay[0-(ms), 1 unit]
The time between matching the images and emulating the key.\
It is used when ```T``` = 1,2,3.

　
### C.Al.(Color Allowance)[0-128]
If you are using method related with RGB, you can specify the tolerance. The smaller the value, the harder the judgment.


　
### Seek[0-(s), 0.01 unit]
Specify seek time of movie after image matching. \
Not set with ```-1```.


　
### Rval, Gval, Bval (value)
Used when the monitoring method is 4 or 5.\
Judgment is made based on whether the RGB value specified here occupies a ratio above the threshold value within the range specified by PX/PY/SX/SY.

　
### AKAZE 
Used when the monitoring method is 9(AKAZE).\
Extract the feature points of the video and template image and calculate the distance between the feature points. If the distance is less than or equal to the value specified here, it is judged to be the same feature point.

Judgment is made based on whether the number of points judged to be the same feature points exceeds the threshold value.

　
### G.C. , G.R. , G.V. (Graph Count/Rate/View) 
This item is related to the graph showing the number of successes and the success rate.

G.C. : Record the number of successes\
G.R. : Record the success rate\
G.V. : Setting whether to reflect the number of successes in the graph or LiveSplit.

0. No
1. Yes

{{<hint info>}}
```G.C``` and ```G.R``` are initialized every time monitoring is started.
{{</hint>}}

　
### PX, PY, SX, SY   
If a monitoring method other than 1 or 9 is specified, the range specified here will be monitored.\
It is automatically entered when creating a template image.


{{< figure src="/image/ash/table006.png" class="center" >}}

　
### PX(S), PY(S), SX(S), SY(S)
Parameters related to scene changes.\
When the images are matched and Timing is set to 2, it monitors whether a scene change has occurred within the range specified here. By default, it monitors the central 40x40 range of the monitoring range.

Detailed settings related to scene changes can be found in [Monitoring Settings]({{< ref "/docs/06eachsettingitem/001monitoring.en.md" >}}).

The range is specified in the same way as PX, PY, SX, SY.

　
### LTX, LTY, RBX, RBY 
Parameters related to limited search. Used when the monitoring method is 1.\
When the images match, the judgment will occur if the template image exists within the range specified here.


{{< figure src="/image/ash/table007.png" class="center" >}}