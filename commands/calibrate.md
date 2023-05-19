---
description: How to use the calibrate command.
---

# calibrate

STOP!

Before proceeding, ensure that the system is in calibration mode and that the motors will not run. This is done by pressing CTRL+C on the Python interpreter. The screen will let you know that the system is in calibration mode and the motors will not run until you exit.



Once in calibration mode, go to the serial monitor to use the command line.

To use the `calibrate` command, type `calibrate` and include the ISE you want to calibrate, such as `calibrate K` to calibrate the Potassium ISE.

Valid arguments are:

* `K` for Potassium
* `NO3` for Nitrate
* `Ca` for Calcium
* `Mg` for Magnesium

pH, DO, EC, and Temperature sensors are presumed to be calibrated within the code and are not available for manual calibration at this time.&#x20;
