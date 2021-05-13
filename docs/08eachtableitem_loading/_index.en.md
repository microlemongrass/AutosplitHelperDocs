---
weight: 80
bookFlatSection: true
title: "Table description [Load remover]"
---

{{<hint info>}}
The maximum number of template images that can be used in Load remover is 30.

Each template image has a timer that (re)starts when positive matching occurs and stops when negative matching occurs (or when the specified template image causes a positive matching reaction).

This timer is used not only for simple load time measurement, but also when, for example, there is a blackout screen before the "Now Loading" characters are displayed and you want to recognize that part as the load time.
{{</hint>}}

{{<hint info>}}
It is highly recommended to use LiveSplit if you want to use the Load remover feature. When using LiveSplit, you should specify a Gametime for Compare Against, and use 5 and 6 (with Gametime) when sending hotkeys to pause/resume time.

If you use other timers, use 1 and 2 in the hotkey transmission.

{{</hint>}}

flowchart
{{< figure src="/image/ash/table_loading001.png" class="center" >}}


{{<hint info>}}
In: Items related to the process that takes place when a template image is matched (positive matching).
Out: Items related to the process that takes place when a template image is no longer matched (negative matching).

Items marked with ```Flag``` are items that specify conditions.
{{</hint>}}


### No
Serial number. Do not change.

### Enable
Specify whether to use.\
　0: Do not use.\
　1: Use.

　
### Comment
Comment.

　
### InFlag_No
Specify the conditions necessary to generate positive matching judgment.
- -1: No additional conditions (threshold only)
- 1-30: Specify from 30 template images (based on ```No```).


　
### InFlag_S(In Flag Status)
Checks the status of the template image specified by ```InFlag_No``` and generates a positive matching judgment in the following conditions

- 0: The target template image does not have any positive matching response.
- 1: The target template image is positively matched
- 2: The target template image has responded to positive matching at least once and is currently unresponsive.

　By setting ```Init```, you can reset the state 2 to 0.


　
### InFlag_Key_No
Specify the conditions necessary to send a hotkey after positive matching judgment occurs.

- -1: No condition
- 1-30: Specify only one of the 30 template images (based on [No]).

　
### InFlag_Key_S(In Flag Key Status)
Checks the status of the template image specified by ```InFlag_Key_No``` and generates a positive matching judgment in the following conditions\

- 0: The target template image does not have any positive matching response.
- 1: The target template image is positively matched
- 2: The target template image has responded to positive matching at least once and is currently unresponsive.

　By setting ```Init```, you can reset the state 2 to 0.

　
### InKey
Specify the signal to send

- -1：Do not send anything
- 0：Split
- 1：Pause
- 2：Resume
- 3：Undo
- 4：Skip
- 5：Pause(Gametime)
- 6：Resume(Gametime)
- 7：Reset


　
### InFlag_LS_No(In Flag LiveSplit No)
Specifies the conditions necessary to change the elapsed time of LiveSplit after positive matching judgment occurs.

- -1: No condition
- 1-30: Specify only one of the 30 template images (based on ```No```).


　
### InFlag_LS_S(In Flag LiveSplit Status)
Checks the status of the template image specified by ```InFlag_LS_No``` and generates a positive matching judgment in the following conditions

- 0: The target template image does not have any positive matching response.
- 1: The target template image is positively matched
- 2: The target template image has responded to positive matching at least once and is currently unresponsive.

　By setting ```Init```, you can reset the state 2 to 0.

　
### InLS_No(In LiveSplit No)
Specifies which template image load time is added to or reduced by the elapsed time of LiveSplit.

- 0: not used.
- 1~ 30: Add the load time of the target template image
- -1~-30: Reduce the load time of the target template image

　
　
### InLS_Time(In LiveSplit Time) (±0.01~ [s])
Adds or subtracts the specified time to the LiveSplit elapsed time.\
If you do not want to change the elapsed time, set this to 0.


　
=================================================================================

### OutFlag
Specifies the condition under which the timer is stopped.

- 0: Until a negative matching response is triggered.
- 1: Until the target template produces a positive matching response.


　
### OutFlag_Tpl
Specify the "target template" for OutFlag from 30 template images (based on ```No```).


　
=================================================================================

### OutFlag_No
Specifies the conditions necessary to generate negative matching judgment.
- -1: No additional conditions (threshold only)
- 1-30: Specify from 30 template images (based on ```No```).


　
### OutFlag_S
Checks the status of the template image specified by ```OutFlag_No``` and generates a positive matching judgment in the following conditions

- 0: The target template image does not have any positive matching response.
- 1: The target template image is positively matched
- 2: The target template image has responded to positive matching at least once and is currently unresponsive.

　By setting ```Init```, you can reset the state 2 to 0.


　
### OutFlag_Key_No
Specifies the conditions necessary to send a hotkey after negative matching judgment occurs.

- -1: No condition
- 1-30: Specify only one of the 30 template images (based on ```No```).


　
### OutFlag_Key_S
Checks the status of the template image specified by ```OutFlag_Key_No``` and generates a positive matching judgment in the following conditions

- 0: The target template image does not have any positive matching response.
- 1: The target template image is positively matched
- 2: The target template image has responded to positive matching at least once and is currently unresponsive.

　By setting ```Init```, you can reset the state 2 to 0.


　
### OutKey
Specify the signal to send

- -1：Do not send anything
- 0：Split
- 1：Pause
- 2：Resume
- 3：Undo
- 4：Skip
- 5：Pause(Gametime)
- 6：Resume(Gametime)
- 7：Reset

　
### OutFlag_LS_No
Specifies the conditions necessary to change the elapsed time of LiveSplit after negative matching judgment occurs.

- -1: No condition
- 1-30: Specify only one of the 30 template images (based on ```No```).

　
### OutFlag_LS_S
Checks the status of the template image specified by ```OutFlag_LS_No``` and generates a positive matching judgment in the following conditions

- 0: The target template image does not have any positive matching response.
- 1: The target template image is positively matched
- 2: The target template image has responded to positive matching at least once and is currently unresponsive.

　By setting ```Init```, you can reset the state 2 to 0.


　
### OutLS_No
Specifies which template image load time is added to or reduced by the elapsed time of LiveSplit.

- 0: not use.
- 1~ 30: Add the load time of the target template image
- -1~-30: Reduce the load time of the target template image


　
### OutLS_Time (±0.01~ [s])
Adds or subtracts the specified time to the LiveSplit elapsed time.\
If you do not want to change the elapsed time, set this to 0.


　
### Delay (0- [ms])
Specifies the amount of time between the occurrence of a negative matching reaction and processing.


　
### Init(Initialize)
Change the status of each template image from 2 to 0 (multiple selections possible).
To select more than one, separate them with an underscore (```_```).\
Example: ```1_2_3```

　
### Others
Same as Split / Reset.



