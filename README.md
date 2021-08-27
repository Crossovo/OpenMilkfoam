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


## Functions we need
The device should offer the same functionality with the Arduino. There are 3 different programmes:

- Cold milk foam
- Milk foam warm
- Milk foam hot

The selection takes place via a single button.

| Modus  | Heater | Motor  | Duration (sec) |
| ------------- | ------------- | ------------- | ------------- |
| Cold milk foam  | off  | on  | 60  |
| Milk foam warm  | on (?? sec)  | on  | ???  |
| Milk foam hot  | on (?? sec)  | on  | ???  |
