---
title: Virtual Capture
weight: 2
bookToc: false
---

# Virtual Capture

{{<hint info>}}
This item must be set when the capture method is set to Virtual.
{{</hint>}}

{{< figure src="/image/ash/setvirtualcapture001.png" class="center" >}}

Usage example (OBSStudio x OBS-VirtualCam)
{{< youtube 6uRJ-58HcMg >}}



(1) Specify the virtual device settings (virtual device to be used, Input resolution, frame rate), and (2) Specify the resolution (```View resolution```) for actual monitoring processing. If ```Cropped``` is specified as the ```View resolution```, the size after cropping is used.

Devices that have been confirmed to work
- SCFH DSF
- SCFF DSF
- XSplit Broadcaster
- NDC (XP)
- Amarek TV V3.1, V4
- OBS Studio (when installing OBS VirtualCam) \
*OBS Studio native virtual webcam does not work.

\
After setting the virtual device, press ```Connect``` to connect to the virtual device.


{{<hint info>}}
- Performance is best when ```Input resolution``` = ```View resolution```, so set it that way if possible.
- Input resolution and output resolution can be added by editing the relevant part in ```savedata/Base.ini``` file.
{{</hint>}}

{{<hint warning>}}
If the connection with the virtual camera becomes unstable, try to disconnect and reconnect.
{{</hint>}}

{{<hint danger>}}
We have confirmed the problem of freezing when connecting to SCFF DSF after connecting to another device. Please save the profile and restart ASH before changing.
{{</hint>}}

　
### Cropping
If there is a black band or other part you want to erase in the captured video, you can delete the corresponding part by checking ```Cropping``` and specifying the cropping range from ```Setting```.

{{< figure src="/image/ash/setvirtualcapture002.png" class="center" >}}


{{<hint info>}}
It is desirable that only the game screen is displayed after capturing/cropping.
- If the display position or size of the game screen changes due to software updates, etc., you can handle it by adjusting the crop.
- It is easy to create the same capture state when sending profile data to other.
{{</hint>}}

{{<hint warning>}}
*If you try to refer to the crop area outside the range of the virtual camera, ```Bad cropping!``` Will be displayed. Make sure the crop area is within range.
{{</hint>}}