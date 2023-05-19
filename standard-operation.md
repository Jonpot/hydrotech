---
description: To operate the HYDRO system normally, follow these steps.
---

# Standard Operation

1. Check that the power is off by looking for a green light on the Arduino in the gray box.
2. Ensure that the ISEs are mounted in the actuation bar are are positioned at the maximum height above the hole in the maintank.
3. Check that the nutrient stock tanks are empty (or, at least, that the pipes are removed from the tanks).
4. Turn on the system. This is usually done by flipping the red switch on the yellow power splitter behind the gray box.
5. Wait for the system to boot. The system is done booting when the screen shows the desktop.
6. Turn the dials for all the pump motor governors and stepper motor power supply to full power.
7. Using the keyboard and mouse, open the Arduino Serial Monitor. This is done by booting the Arduino IDE and clicking the magnifying glass in the top right.
8. Enter the command `full_test` and press enter.
9. This will launch the system into a full test of all capabilities, verifying the vertical range of the motors, obtaining values from all sensors, and turning all pumps on for 1 second. If there are any abnormalities during this step, you should stop and perform repairs.
10. After the test is completed with no abnormalities, replace the tubes into the stock solutions/make solutions and fill the stock tanks.&#x20;
11. Run the main\_1.py file on the RaspberryPi. You will be prompted to enter in some values. You can press enter to skip entering a value and take the defaults:
12. Large Tube Flowrate: 13.875 \[mL/s]
13. Small Tube Flowrate: 18.594 \[mL/s]
14. Volume: 10,000 \[mL]
15. Ideal pH: 6
16. All Nutrient Setpoints: 200 \[ppm]
17. Automated B Solution Volume: 0 \[mL]
18. pH Stock Concentration: 0.2 \[pH/mL]
19. All Nutrient Stocks: 100 \[ppm]
20. Wait time: 3 \[hours]
21. After all the parameters have been entered, you will be prompted to use the command line to calibrate all the ISEs. Use the [calibrate](commands/calibrate.md) command to calibrate your ISEs, then return to Python and press enter.
22. The system is now running! It will immediately raise the water level to the ideal height, lower the sensors into the solution, take measurements, then raise the sensors, and use the pumps to balance the solution. This will repeat whenever the specified wait time is completed.
23. At this point, you may also turn on the water circulation and lighting systems, which are considered seperate from the HYDRO device.
