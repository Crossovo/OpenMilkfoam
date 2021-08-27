# jura_milkfrother
Defects usually come from the electronics. We implement a new one based on the Arduino (8Bit).

## Background
The milk frother has a good hardware base but unstable electronics. Most defects come from the electronics.

I don't want to throw the appliance away just because the electronics fail.

Hence this project.

There are 2 circuit boards in the unit. A control board with the uC on it, the push button input and 3 LEDs for the selection made.

A power electronics board with relays for the heater and the 5V power supply for the control board. This board is provided with sufficient protection elements (temperature monitor, fuse which trips in case of overtemperature) to protect the unit for thermal overloads.

This base is good.
