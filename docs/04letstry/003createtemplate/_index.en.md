---
weight: 12
bookToc: false
title: "Create Template Image"
---

# Create Template Image

Create an image to use as a template in image recognition.

Select ```Tool``` → ```Create preview / template image``` to move to the screen to create a template image.

{{< figure src="/image/ash/preview001.png" class="center" >}}

{{<hint danger>}}
- The first row of the table is reserved for "Reset". Normal monitoring is used from the second line.
- Create a template for "Reset" even if you do not use "Reset" monitoring.
- Also, even if you want to execute "Loop" processing, create two templates for Split (up to the third row in the table).
{{</hint>}}


## How to create a template image

1. Specify the monitoring method from the [Method] box. There are several types of monitoring methods. This time, specify [8: L2Norm].

2. Before capturing the image, click on the left side of the table to make it "row selected". The parameters are saved in the selected row.

3. When the scene you want to use as a template is displayed, click [**Capture**] button. The image at the time of pressing remains, so click and drag to select the region you want to use as a template.



{{<hint info>}}
Check [**Full screen**] and press the [**Capture**] button to capture the entire screen.
{{</hint>}}
\
\
\
*Additional processing may be required depending on the method selected. Please follow the instructions on the screen.


{{<hint info>}}
- Scene suitable as a template is a scene where the image is not flat, a unique scene (score result, characteristic icon displayed when clearing, etc.).
- Mask processing may be required depending on the template (example: "SHINE GET!" Display of Super Mario Sunshine). See [Using Mask Images]({{< ref "/docs/10tips/009maskimage.en.md" >}}) for details.
{{</hint>}}

{{<hint info>}}
If you specify ```Template matching``` in Method and check [**Limit**], you will be asked to select the range again after capturing the template. The range specified here is used to check if the matched image is within that range.
{{</hint>}}

{{<hint info>}}
You can create the template image while playing the game, and you can also capture the recorded video first, create the template image, and then set it to capture the game screen again. In this case, **please select display resolution other than "Cropped"**.
{{</hint>}}


### Method
Specifies which method is used to calculate the similarity. Corresponds to ```Met.``` column of the table. For a description of each method, refer to [Characteristics of each monitoring method]({{< ref "/docs/10tips/007monitoringmethod/_index.en.md" >}}).

Basically, if you use either ```Template matching``` / ```L2 Norm```, you can use it in most situations.

{{<hint info>}}
- When the position where the image is displayed is always fixed → L2Norm
- When the position where the image is displayed is random and changes depending on the player's operation → Template matching
{{</hint>}}


### Replay function
If the scene you want to use as a template is displayed only for a moment or only while operating the game, it will be difficult to create a template.\
If you press [**Replay**] button, you can display the latest video again, and you can capture even such a scene.\
The retention time of the replay video can be specified on the [Other] tab of the settings.

{{< figure src="/image/ash/preview002.png" class="center" >}}

### Create template image for Load Remover
If you check [**For Load Remover**], the table will switch and you will be able to create a template image for Load Remover (file name: loading[n].png). There is no change in the method of creating template images.

### Target
Specify the capture target (Video/Audio).

### Similarity check
If you check [**Similarity**], the similarity between the "image corresponding to the currently selected row" and the "captured video" will be calculated. It is used to check whether the template can be used without problems.

{{< figure src="/image/ash/preview003.png" class="center" >}}

[Current similarity] [Maximum similarity] is displayed.

{{<hint warning>}}
*If ```filter``` is applied, the setting will be reflected, but the template cannot be captured.
{{</hint>}}