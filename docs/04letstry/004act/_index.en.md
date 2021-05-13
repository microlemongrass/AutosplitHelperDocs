---
weight: 13
bookToc: false
title: "Start Monitoring"
---

# Start Monitoring

## To start monitoring
Press [**Start**] button to start monitoring.\
If the settings are incorrect, an error message will be displayed. Please correct the settings according to the display.


{{< figure src="/image/ash/monitor002.png" class="center" >}}

% Display
Above: Current similarity
Below: Maximum similarity

**When the similarity exceeds the threshold (the number on the right), it is judged as a match.** 

When an image match judgment occurs, "Match" is displayed and a split signal etc. is sent (additional processing may be performed depending on the settings).

"Finish" is displayed when all monitoring is completed.

{{<hint info>}}
Even if reset monitoring is enabled, reset monitoring will end after "Finish". If you want to continue monitoring the reset (start the next measurement without operating ASH), refer to [Restart after monitoring finish]({{< ref "/docs/10tips/001afterfinish.en.md" >}}).
{{</hint>}}

The box to the right of the similarity display allows you to check the similarity of other images when using multiple simultaneous monitors.

The number to the right of "Load" shows the value related to the delay of key transmission.

The timer on the right is for load removal. Shows the load time and cumulative load time.

## About various buttons
### Stop
The image recognition process ends.

### Small / Large
Simplify the window. The CPU load is slightly reduced because the preview is stopped.

### [| ←, ←, →]
Reset, Undo, and skip, respectively.
If you check "Interlock" in the HotKey setting, it will be linked with the timer.

### Details
If you are using multiple simultaneous monitors, the similarity of each template is displayed at once.

### AKAZE Result
If AKAZE is specified as the monitoring method, the result image of AKAZE is displayed.