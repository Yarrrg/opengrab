# OpenGrab Electro Permanent Magnet #

EPM688-V2.X,

## General Description ##
<img width='400' align='right' src='http://i.imgur.com/xoVx6k9.jpg' />

The EPM688-V2.X is an Electro Permanent Magnet, combining the advantages of electro and permanent magnets. This Device comes with integrated electronics that can be operated with 5V PWM signal common on RC electronics. The device is designed to hold 1kg of cargo. It is the users responsability to verify that this can be achieved in each particular case.



## Applications ##
  * Robot arm work holding
  * Cargo lift for UAV's
  * Educational demonstration of magnetic properties


&lt;BR&gt;



&lt;BR&gt;



&lt;BR&gt;



&lt;BR&gt;



&lt;BR&gt;



&lt;BR&gt;



&lt;BR&gt;



&lt;BR&gt;



&lt;BR&gt;



&lt;BR&gt;



&lt;BR&gt;



&lt;BR&gt;


<img width='400' align='right' src='http://i.imgur.com/lSxJCyV.jpg' />
## Features ##

  * CanAerospace Daughter card is available
  * 5V Vcc
  * PWM signal
  * Minimal steady state power <1mW
  * Water resistant conformal coating
  * 300ms Cycle times
  * On board Pic12F with source code and in-circuit programming header


## Recommended Operational Conditions ##

| **Symbol** | **Parameter** | **Rating** | **Units** |
|:-----------|:--------------|:-----------|:----------|
| Vcc max    | Power supply Voltage max | 7          | V         |
| Vcc min    | Power supply Voltage min | 3.3        | V         |
| Imax       | Maximum Supply Current | 600        | mA        |
| PWM on     | Minimum signal high | 1.75       | ms        |
| PWM off    | Maximum signal high | 1.25       | ms        |
| PWM error  | PWM out of range | <0.75-2.25< | ms        |
| Tmax       | Maximum Temperature | 80         | deg C     |
| Tmin       | Minimum Temperature | -40        | deg C     |
| Tcharge    | Charge time (1) | 300        | ms        |
| Fmax       | Max holding force | 60         | N         |
| Mass       | Mass          | 47         | gram      |


(1) at 5V Vcc


## CanAirospace Daughter card ##
<img width='400' align='right' src='http://i.imgur.com/asZxqiV.jpg' />
OpenGrab CAN Daughterboard (OGCAN) provides CAN interface for OpenGrab EPM. Hardware part of this interface follows the UAV CAN convention (see "Hardware Interconnection"). As for protocol, currently only the CANaerospace protocol is supported (via libcanaerospace). Full support for UAV CAN is scheduled to be implemented by March or April 2014. Generally, OGCAN is the first commercially available piece of hardware that follows the UAV CAN RFC.
For more information please see: https://docs.google.com/document/d/1Ybt6NxST_QbpNfdEGE-l7oGNAbfmcufVGxpM0q9ekjc/pub
## Pin Functions ##

### GND ###
Ground pin
### VCC ###
5V supply <100mV ripple
### PWM ###
RC PWM signal input


### Data ###

The Data pin puts out the current state of the EPM, TTL high for On and TTL low for Off.

### VPP PGD PGC ###
These pins are broken out to provide the user with the ability to reprogram the on board PIC12F. Further information can be found in the documentation provided by Microchip


### Operation ###

After connection VCC and GND the device will start charging the main capacitor. This takes around 300ms at 5V Vcc. After the charge is complete the EPM is ready to go in either the On or Off state. After a command has been issued there is a 300ms delay before the next switching command is accepted to ensure that the capacitor is charged. When operating at low voltages care must be taken to allow sufficient time for the charging to complete.

## Push Button Mode ##

Pressing the Push button will toggle the EPM

## PWM Mode ##
A RC Pulse Width Modulated signal can also be used.
High times between 0.75 and 1.25ms are consider an Off command. 1.75-2.25ms is considered On command.
Moving the signal on time from neutral, 1.25-1.75ms to either On or Off range will command the EPM to go into the respected state.

## Error ##
The Led will blink once every 64 PWM signal errors. An error is either a missing or out time range PWM, about every 2 seconds for a missing PWM.

## LED ##
Led goes on when the button is pressed.
The Led will blink rapidly 6 times after a command has been executed, either going On or Off.





## Drawing ##
http://opengrab.googlecode.com/files/EPM%20688%20V2.pdf
<img width='500' align='right' src='http://i.imgur.com/6PJNapw.jpg' />

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