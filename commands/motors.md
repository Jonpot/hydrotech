---
description: How to use the motors command.
---

# motors

```
> #### warning::STOP!
>
> Before proceeding, ensure that the system is in calibration mode and that the motors will not run. This is done by pressing CTRL+C on the Python interpreter. The screen will let you know that the system is in calibration mode and the motors will not run until you exit.
```





Once in calibration mode, go to the serial monitor to use the command line.

To use the `motors` command, type `motors` and include the axis you want to move and the distance you want to move, preceded by `reps:`, such as `motors horizontal reps:100` to move the horizontal motors by 100 units.

The safe stroke length for the vertical motors is 5000 reps. The safe stroke length for the horizontal motors is 700 reps.

Be sure to move the motors back to their default resting position before exiting calibration mode.

Once the motors have returned to their default positions, type "exit" into the Python interpreter to exit calibration mode. Motors may move immediately if another rebalancing was scheduled during the calibration.
