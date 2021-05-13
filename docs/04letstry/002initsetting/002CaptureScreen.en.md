---
title: Screencapture setting
weight: 2
bookToc: false
bookFlatSection: true
---

# Screencapture setting

You can specify the screen capture target, resize, and crop here.\
\
See [Screen Capture]({{< ref "/docs/06eachsettingitem/003screencapture.md" >}}) for details on each setting.


**Type** specifies ``` Window```, and in the list below, specify ```Windowed Projector (Preview)```.

After completing the settings, press **Initialize rect**. This completes the setting to capture the entire screen of the windowed projector.

{{<hint info>}}
The initial size of the window projector is 480x270, which is not saved when resized. If you want to display in a large size, we recommend to use [Position Setting]({{< ref "/docs/10tips/008positionsetting/_index.en.md" >}}) or use the following software.
{{</hint>}}
[OBS Window Projector Reszier](https://booth.pm/ja/items/2057279)\
\
Next, set **Cropping**. Use this when the captured image has a part other than the game screen such as a black belt.\
[Cropping]({{< ref "/docs/06eachsettingitem/003screencapture/_index.en.md#クロッピング" >}})\
\
\
Finally, **Specify the display resolution**. This is the resolution when processing on ASH. The appropriate resolution depends on "game content", "ASH settings", and "PC specifications".\
Basically, choosing "Cropped" will give you the best accuracy.\
If the target you want to use as a template is small / fine, we should increase the display resolution, and if you want to reduce the load, decrease the display resolution.