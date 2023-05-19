---
description: How to use the full_test, sensor_test, motor_test, and pump_test commands.
---

# <>\_test

{% hint style="info" %}
## STOP!

Before proceeding, ensure that the system is in calibration mode and that the motors will not run automatically. This is done by pressing CTRL+C on the Python interpreter. The screen will let you know that the system is in calibration mode and the motors will not run automatically until you exit.
{% endhint %}

To use the `<>_test` command, go to the serial monitor to use the command line and type the command for the subsystem you'd like to test.

Valid commands are:

* `full_test`, which runs `motor_test`, then `sensor_test`, then `pump_test`. **This command moves the motors.**
* `motor_test`, which attempts to actuate the sensing bar all the way down the vertical stroke length, then all the way back up. **This command moves the motors.**
* `sensor_test`, which attempts to read values from all of the sensors (note that they may or may not be submerged). This uses the currently stored calibration equation.
* `pump_test`, which attempts to turn each of the pumps on for one second, then turns them off.

Once the motors have returned to their default positions, type "exit" into the Python interpreter to exit calibration mode. Motors may move immediately if another rebalancing was scheduled during the calibration.
