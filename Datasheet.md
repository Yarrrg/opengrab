# OpenGrab Electro Permananet Magnet #

EPM688-5, EPM688-5-S, V1.0X, V1.2

## General Description ##

The EPM688-5 and EPM688-5-S are Electro Permanent Magnets, combining the advantages of electro and permanent magnets. This Device comes with integrated electronics that can be operated with 3.3 and 5V TTL signals and uses 5V Vcc.

<img width='400' align='right' src='http://i.imgur.com/vkteLjs.jpg' />
## Applications ##
  * Robot arm work holding
  * Cargo lift for UAV's
  * Educational demonstration of magnetic properties

## Features ##

  * 5V Vcc
  * 3.3 or 5V TTL signal
  * Minimal steady state power <1mW
  * Water resistant conformal coating
  * 330V shocks are possible when touching the unit (patent pending auto weakup feature)




## Recommended Operational Conditions ##

| **Symbol** | **Parameter** | **Rating** | **Units** |
|:-----------|:--------------|:-----------|:----------|
| Vcc min    | Power supply Voltage  | 5          | V         |
| Vcc min V1.2 | Power supply Voltage min | 3.3        | V         |
| Vcc max    | Power supply Voltage max| 6          | V         |
| Imax       | Maximum Supply Current | 1.5        | A         |
| Vsig low   | Maximum low signal Voltage [1](1.md) | 2.2        | V         |
| Vsig high  | Minimum high signal Voltage [1](1.md) | 2.8        | V         |
| Vsig max   | Maximum signal Voltage | 5          | V         |
| Tmax       | Maximum Temperature [2](2.md) | 50         | deg C     |
| Tcharge    | Charge time   | 3          | s         |
| Fmax       | Max holding force | 80         | N         |
| Mass       | Mass          | 55         | gram      |




[1](1.md) Vsig is undefined between 2.2 and 2.8V. **V1.0 and V1.1 only** Operating the signals this area may cause premature turn off of the IGBT under high current conditions causing permanent damage. Oscillation on either the Vsig Vcc may cause rapid turn off and on of the IGBT. This can be avoided by using a clean power supply. http://www.nxp.com/documents/data_sheet/74HC_HCT32.pdf 4HC\_HCT32.pdf] should be consulted.
This is not a problem with V1.2 which will not suffer damage from noise.


[2](2.md) Without electrolyte capacitor 80 deg C


## Pin Functions ##

### Gnd (Pin 1 and 6) ###
Ground pin
### Vcc (Pin 2 and 5) ###
5V supply <100mV ripple
### S\_off (Pin 3) ###
This turn off pin has two functions, to charge the capacitor and to turn off the EPM.
The EPM can only switch when the capacitor is charged.
To operate the EPM Pull this pin high (it has a 1kohm pull down) for 3 seconds. This will charge the capacitor. Now that the capacitor is charged the EPM is ready to cycle or switch.
Pull this pin high again and it will switch into it's off state.

The relative high self discharge rate of the capacitor should be taken into account, eg it is recommended that the time between charge and switch is less then 60 seconds.

### S\_on (Pin 4) ###

Same as S\_off (except it turns the EPM on)

### Gehäuse 1-6 ###
Breakout of the 6 contact points for use for electrical contact.
The 6 individual metal contacts on the bottom are broken out so one may solder a connector to the board. This is intended to be used with a recharge station.

## Operation ##

The EPM688-5 is designed to hold securely a cargo of 1kg and switch on and off effectively  with low power consumption. 800mA at 5V for 3S  or 3.4J per cycle.

Under the capacitor discharge condition pull either S\_on or S\_off high >2.8V for 3 seconds and then low. The capacitor is fully charged and the device is ready to cycle. Pulling either S\_on or S\_off high causes the magnetic field to move either in the on or off state. Care should be taken that the S\_on or S\_off are set high for no less then 500uS otherwise IGBT turn off under high current condition can cause damage.
Pulling S\_on or S\_off low after >500uS have expired causes the driver to charge the capacitor, automatically stopping once 330V is reached in about 3s.


## Drawing ##
<img width='500' align='right' src='http://i.imgur.com/CgFtE4d.jpg' />

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>