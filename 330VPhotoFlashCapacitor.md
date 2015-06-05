# 330V PhotoFlash Capacitor Charger 3.6V input #

CT330

## General Description ##

The CT330 is a 330V power supply based on LTs LT3485-3 Fly Back Driver for use as a capacitor charger. Capable of 8mA @ 330V ouput from a single cell lithium battery Vin 3.6V. Typical charge time is 50ms per uF of capacitance. The CT330 can operate continuously at Vin <4V

<img width='600' align='right' src='http://i.imgur.com/lx97Tav.jpg' />
## Applications ##
  * Coil Gun Capacitor charger
  * Power supply 330V from a single cell lithium battery
  * Shocking people

## Features ##

  * 2.5-10V
  * 3.3 or 5V TTL signal
  * Minimal steady state power <1mW
  * Water resistant conformal coating
  * 330V shocks are possible when touching the unit (patent pending auto weakup feature)




## Recommended Operational Conditions ##

| **Symbol** | **Parameter** | **Rating** | **Units** |
|:-----------|:--------------|:-----------|:----------|
| Vcc        | Power supply Voltage  | 3.6 - 10   | V         |
| Imax       | Maximum Supply Current | 1.5        | A         |
| Vsig low   | Maximum low signal Voltage  | 0.3        | V         |
| Vsig high  | Minimum high signal Voltage | 1          | V         |
| Vsig max   | Maximum signal Voltage | 10         | V         |
| Tmax       | Maximum Temperature [2](2.md) | 80         | deg C     |
| Tcharge    | Charge time 50uF | 2.5        | s         |
| Mass       | Mass          | 3.7        | gram      |

Care should be taken to avoid overheating at Vin over 4V. Although for a typical charging application the device can operate well above 4V since the time is limited. Above a few hundred uF care must be taken.


## Pin Functions ##

### GND ###
Ground pin
### Vcc ###
Supply
### Sig Charge ###
Pulling this pin high (1 kohm pull down) causes the CT330 to charge. Operation will terminate when 330V is reach or this pin goes low

### Sig Out ###

Broken out pin intended to drive an Tyristor or similar device

### Rshunt ###

Broken out pins intended to be use whit a current sensing shunt

### 330V out ###
High voltage output


## Diagram ##
The design is open source and available at http://upverter.com/ctech4285/a9f9b3badea506e9/330V-power-supply