---
title: ClearCheacker
weight: 13
bookToc: false
---

# ClearChecker

{{<hint info>}}
Items related to Clear Checker.
{{</hint>}}


{{< figure src="/image/ash/setclearchecker001.png" class="center" >}}

This is similar to the clear checker in "Kirby's Air Ride".\
You can use it by checking ```Use clear checker function"```.



This function makes a list of the registered template images and displays the specified image when the template images match.

## How to register images
Create a template image using ```Preview / Create Template Image```.

Set the value of ```No``` column corresponding to the template you want to monitor in the table to ```1```, enable ```Loop``` in the monitoring settings, and set the number of loops to the number of templates you want to monitor.\
You can make settings related to loops by pressing ```Apply Setting```.


### Path
Specify the image to be displayed when the template image is matched.\
Create a folder containing the number of images to be displayed when the template image is matched, and the background images, and specify the folder.

　　1.png\
　　2.png\
　　...\
　　background.png

### Number of images to be displayed in one line
When the template image is matched, the image displayed will be overlaid on the background image.
At this time, specify how many images will be placed in one line.


### Image's size
The size of each image. If you use an image that is not of this size, it will be resized.


### Columns x Rows
The number of images per row and per column to be displayed on the background image.


*In the list view, the text entered in ```Comment``` column of the table will be displayed.