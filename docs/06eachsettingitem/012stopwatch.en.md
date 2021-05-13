---
title: Stopwatch
weight: 12
bookToc: false
---

# Stopwatch
画像画像画像

{{<hint info>}}
Items related to the stopwatch. ```Comment``` columns in the table are relevant to this item.
{{</hint>}}

## Stopwatch

{{< figure src="/image/ash/setstopwatch001.png" class="center" >}}

Set the font name, font size, format, Startat and press ```Show``` to display the stopwatch window.


The stopwatch starts and stops when the string entered in ```Comment``` column of the table contains ```_start_``` and ```_stop_```.

{{< figure src="/image/ash/setstopwatch002.png" class="center" >}}


## Table
Records various information such as segment time.

### How to use
- After opening the Table window, right-click on the table and select ```Initialize```.
At this time, ```_start_``` and ```_stop_``` must be described in ```Comment``` column of the table in the main window.

- When you keep the Table window open while monitoring, the time will be recorded automatically.

### About BestSplitTime
This function is different from the BestSplitTime of LiveSplit.
If ```Comment``` column in the table contains ```_bst_```, the best record up to that line will be saved.

  
In the following case, the best record of sections 1-3 will be saved in "xx", and the best record of sections 4-6 will be saved in "yy".

  Comment | ... | BST
----------|-----|---------
  1       | ... | --
  2       | ... | --
  3_bst_  | ... | xx
  4       | ... | --
  5       | ... | --
  6_bst_  | ... | yy
  7       | ... | --