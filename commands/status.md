---
description: How to use the status command.
---

# status

{% hint style="info" %}
## STOP!

Before proceeding, ensure that the system is in calibration mode and that the motors will not run. This is done by pressing CTRL+C on the Python interpreter. The screen will let you know that the system is in calibration mode and the motors will not run until you exit.
{% endhint %}

Once in calibration mode, go to the serial monitor to use the command line.

To use the `status` command type `status`.

This command first checks the water level and fills the tank to the ideal level, drops the ISEs into the solution, takes measurements, extracts the ISEs from the solution, then reports the readings to the serial monitor.



Once the motors have finished moving up, type "exit" into the Python interpreter to exit calibration mode. Motors may move immediately if another rebalancing was scheduled during the calibration.
