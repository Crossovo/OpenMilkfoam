# OpenMilkfroather
Milk frother and OpenSource? Yes indeed, this is a project based on the Jura milk frother Hot & Cold 24019, which hardware is technically OK and the electronics no longer work. The idea is born to bring the hardware back to life - Welcome to OpenMilkfrother.

## Background
The jura milk frother has a good hardware base but in many cases unstable electronics. Most defects come from this electronics.

We don't want to throw the appliance away just because the control board fail.
Replacement Parts are not available on the market. Until now.

## Into the milk frother
There are 2 circuit boards in the milk frother. 

### Boards

#### A control board 
- with the uC 
- one push button for input 
- 3 LEDs for the selection made
- power supply and control of the motor for the rotor

#### power electronics board 220V
- with relays for the heater 
- 5V power supply for the control board
- sufficient protection elements (temperature monitor, fuse which trips in case of overtemperature) to protect the unit for thermal overloads.

### cables and pin seeting
#### from the power electronic board 
There are 4 cables from the power electronic board.

- black - 5V DC
- white - GND
- blue - Input to start the heater
- red - Output from transformer as 1V AC to measure the frequency

#### from the uC Board
- GND
- Input for the Motor (5V)

## Functions we need
The device should offer the same functionality with the Arduino as a one button system.  BUT - I additionaly want to enter 3 differnt milks varieties. 

The selection takes place via a single button.

### The rationale:
- The selection of the type (cold/warm/hot) should be able to be changed at the touch of a button. 
- The type of milk can then set by pressing the button for the desired programme. 


### Modus
| Modus  | Heater | Motor  | Duration (sec) | Target Temperatur | LED |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| Cold milk foam  | off  | on  | 60  | % | 1 |
| Milk warm  | on (?? sec)  | on  | ???  | 50°C | 2 |
| Milk foam hot  | on (?? sec)  | on  | ???  | 60°C | 3 |

With no input, after 2 sec - the device os going to blinking for 

### Milk varieties
| Milk  | LED blinking |
| ------------- | ------------- |
| cow | 1 | 
| almond | 2 |
| out | 3 |

After 5 seconds later or if no further selection has taken place, the programme starts.

There is no direct temperature measurement of the heating or the milk. 
I assume that everything is controlled via timer (the mains frequency is measured at the uC).

## Tasks for the next steps
- how much time need a cold milk (7°C) from the cooler to heat up to different temperatures in the bootle with max laods
- a programm draft sketch in arduino to implement the "core system" for the one button device


### Feature Ideas
- a sensor as input for the liquid temperature in the vessel (sensor must be plugged in externally)
  - warming baby milk (37°C)
  - perfect milk foam (measured not over time)
- Sound for feedback
- ...
