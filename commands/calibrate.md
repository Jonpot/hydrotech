---
description: How to use the calibrate command.
---

# calibrate

{% hint style="info" %}
## STOP!

Before proceeding, ensure that the system is in calibration mode and that the motors will not run automatically. This is done by pressing CTRL+C on the Python interpreter. The screen will let you know that the system is in calibration mode and the motors will not run automatically until you exit.
{% endhint %}

Once in calibration mode, go to the serial monitor to use the command line.

To use the `calibrate` command, type `calibrate` and include the ISE you want to calibrate, such as `calibrate K` to calibrate the Potassium ISE.

Valid arguments are:

* `K` for Potassium
* `NO3` for Nitrate
* `Ca` for Calcium
* `Mg` for Magnesium

_pH, DO, EC, and Temperature sensors are presumed to be calibrated within the code and are not available for manual calibration at this time._&#x20;

Once you've sent the command with the specified sensor, you will be prompted to place the ISE in the high-point (1000 ppm) solution and then type "ready". Sending anything else will cancel the calibration. After calibrating the high point, you will be prompted to place the ISE in the low-point (10 ppm) solution and then type "ready". Sending anything else will cancel the calibration, but the high-point will have already been set.



Once you are done calibrating all of your sensors, type "exit" into the Python interpreter to exit calibration mode. Motors may move immediately if another rebalancing was scheduled during the calibration.
