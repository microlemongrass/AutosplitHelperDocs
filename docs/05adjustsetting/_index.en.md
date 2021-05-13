---
weight: 50
bookFlatSection: true
title: "Adjust Setting"
---

## Adjust setting (when matching judgment does not occur)
Matching judgment may not occur normally with only the settings made so far. The following is a list of possible troubles and remedies.

### Trouble with monitoring fps
If the template image is a scene where only a few frames are displayed, recognition omission may occur if the monitoring fps is small.\
→ It is recommended to increase the monitoring fps or not to use the target that is displayed only slightly.

　
### Trouble with threshold setting
The threshold usually works normally if you specify around 90%, but in some cases it may be necessary to correct the value (for example, even if the target moves, deforms, scales, or there is a similar target).\
Basically, I would like you to set a template image that is specific and does not move, but if that scene does not exist at all, you may be able to capture it by reducing the threshold value. Also, consider changing the monitoring method.

　
## If you want to adjust the split timing
With ASH, you can adjust the timing of sending the split signal in the following ways.
--Wait for a specified time before sending a signal
--The specified range changes scenes such as darkening + waits for a specified time before sending a signal
--When the images match, wait until they no longer match (negative matching) + wait for a specified time before sending a signal.

By using these, you can adjust the split timing to some extent.

See [here]({{< ref "/docs/07eachtableitem/_index.en.md#ttiming" >}}) for more information.