# jura_milkfrother
Defects usually come from the electronics. We implement a new one based on the Arduino (8Bit).

## Background
The milk frother has a good hardware base but unstable electronics. Most defects come from this electronics.

I don't want to throw the appliance away just because the control board fail. 

Replacement Parts are not available on the market. Hence this project.

## Boards
There are 2 circuit boards in the unit. 

### A control board 
- with the uC 
- the push button input 
- 3 LEDs for the selection made
- power supply and control of the motor for the rotor

### power electronics board
- with relays for the heater 
- 5V power supply for the control board
- sufficient protection elements (temperature monitor, fuse which trips in case of overtemperature) to protect the unit for thermal overloads.

### Cables
### from the power electronic board 
There are 4 cores from the power electronic board.

- black - 5V DC
- white - GND
- blue - Input to start the heater
- red - Output from transformer as 1V AC to measure the frequency

### from the uC Board
- GND
- Input for the Motor (5V)

## Functions we need
The device should offer the same functionality with the Arduino.  BUT - I additionaly want to enter 3 differnt milks varieties. 

There are 3 different programmes:

- Cold milk foam
- Milk foam warm
- Milk foam hot

The selection takes place via a single button.

| Modus  | Heater | Motor  | Duration (sec) | Target Temperatur | LED |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| cow Cold milk foam  | off  | on  | 60  | % | 1 |
| cow Milk warm  | on (?? sec)  | on  | ???  | 50°C | 2 |
| cow Milk foam hot  | on (?? sec)  | on  | ???  | 60°C | 3 |
| almond Milk warm  | on (?? sec)  | on  | ???  | 50°C | 2 | 
| almond Milk foam  | on (?? sec)  | on  | ???  | 50°C | 3 |
| out Milk warm  | on (?? sec)  | on  | ???  | 50°C | 2 |
| out Milk foam  | on (?? sec)  | on  | ???  | 50°C | 3 |


There is no direct temperature measurement of the heating or the milk. 
I assume that everything is controlled via timer (the mains frequency is measured at the uC).

## Tasks for the next steps
- how much time need a cold milk (7°C) from the cooler to heat up to different temperatures in the bootle with max laods
- a programm draft sketch in arduino
