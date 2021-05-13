---
title: Filter
weight: 5
bookToc: false
---

# Filter

{{<hint info>}}
You can set what to do with pre-processing of captured video. This is effective when the following monitoring methods are used.
- Template matching
- AKAZE
{{</hint>}}

{{< figure src="/image/ash/setfilter001.png" class="center" >}}

### Grayscale
Make the video grayscale. Grayscale can be expected to improve processing speed and reduce CPU load.

{{<hint warning>}}
If you use a monitoring method that directly uses RGB values, don't use it because it won't be possible to monitor accurately.
{{</hint>}}

　
### Canny/Binarization
Edge/Binarize video. 

Thia process can reduce the possibility of misrecognition.

　
#### Thr.1 / Thr.2
The minimum and maximum hysteresis threshold values. This parameter is used to determine whether the edge obtained by the preprocessing in Canny is a real edge. The larger the value, the more severe the edge judgment and the number of detail edges is reduced.
　
#### L2
```L1``` is high speed.\
```L2``` is high precision.

In details, please see [Canny - OpenCV documentation](https://docs.opencv.org/master/dd/d1a/group__imgproc__feature.html#ga04723e007ed888ddf11d9ba04e2232de)

　
#### Blocksize
The size of the neighborhood area used for threshold calculation when performing "Adaptive threshold" processing. Specify an odd number greater than 1.

　
#### Parameter
A constant subtracted from the calculated threshold.