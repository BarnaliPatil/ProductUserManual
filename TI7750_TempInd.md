# Product Manual for Temperature Indicator with Alarm - TI7750 #

*Iss 01 Rev 00*                                              
-----------------------------------------------------------------
### Contents ###

| Sr. No. | Topic |
| ----------------------- | ------------------------- | 
| 1 | Introduction |
| 2 | Front Panel Indication |
| 3 | Analog Inputs |
| 4 | Alarm Options |
| 5 | Operation |
| 6 | Installation |
| 7 | Power Connection |
| 8 | Self-Test Error Codes |
| 9 | Indicator Specifications |
----------------------------------------------------------
# INTRODUCTION #

In process control application, sensors are used to measure physical variables such as Level, Temperature, Flow, Pressure, Speed, and Position. Temperature indicators are process control installation instruments that can process signals from temperature sensors and show them on the display.


The TI 7750 is an advanced microcontroller based single channel Process / Temperature Indicator used for monitoring analog signals in the majority of industrial processes.  It can accept mA, mV, Volts, PT100 RTDs and Thermocouple input signals.


Basic input types are selected by on card jumpers and by selecting from the keyboard. Optional single or dual alarm output is provided, alarm type and value are programmable from the front panel keyboard.


Alarm condition on Sensor break, Over range or Under range is programmable individually for each alarm.
Programmable Power On alarm delay timer is provided to inhibit alarm operation for the duration of the delay time.

All programmed values are stored permanently in non-volatile memory. Its intelligent program lock facility prevents the set parameters from being tampered. 

# FRONT PANEL INDICATION #

![TI7750](https://github.com/BarnaliPatil/ProductUserManual/assets/152055230/da9f27ee-90be-4bee-81f0-efe5249839a1)
Fig. 1

2.1 Display : Process Value, 4-digit 7segment Red LED

2.2  13.0 x 8.0mm transparent pocket for legend insertion

2.3   ALARM LEDs
* OP1:  ALARM 1, red color
* OP2:  ALARM 2, red color
      
2.4  Key Switches

# KEY SWITCHES #

The meaning of the symbols on the key switches are listed in figure 2 below,

![KeySwitches](https://github.com/BarnaliPatil/ProductUserManual/assets/152055230/272574bd-a310-439c-ba6b-5e975b7c016f)
Fig.2

# ANALOG INPUTS #

The indicator can accept the following inputs:-

| TYPE | RANGE |
| --------------------------- | ---------------------------- |
| DC mA | 4 to 20 mA |
| DC Volts | 1 to 5V |
| DC mV | 15 to 75 mV|
| RTD | PT100  (Alpha = 0.00385) in  1 Deg resolution |
| Thermocouples | J, K and T |

Table 1

The linear inputs mA ,mV and Volts can be programmed for normal  ZERO and SPAN  or center zero scale or for user 10 segment curve entered from the keyboard. 

The five basic input types are to be selected from the keyboard and appropriate jumpers set on the indicator card.

**WARNING !!   Always check the set internal jumpers before using a input , as wrong jumper settings can damage the input.**

# INPUT SELECTION CODE #

| CODE | INPUT TYPE | INPUT RANGE |
| -------------------- | -------------------- | ---------------------- | 
| 00 | 4 to 20 mA Normal scale | -1999 to +9999 |
| 02 | 4 to 20 mA Centre zero scale | -1999 to +9999 |
| 10 | 1 to 5 Volts Normal scale | -1999 to +9999 |
| 12 | 1 to 5 Volts Centre zero scale | -1999 to +9999 |
| 20 | 15 to 75 mV Normal scale | -1999 to +9999 |
| 22 | 15 to 75 mV Centre zero scale | -1999 to +9999 |
| 30 | RTD PT100, 1 Deg C resolution | -200 to +800 Deg C |
| 40 | Thermocouple Type J | -200 to +1200 Deg C |
| 41 | Thermocouple Type K | -200 to +1372 Deg C |
| 42 | Thermocouple Type T | -200 to +400 Deg C|
| 46 | Thermocouple Type S | -50 to +1768 Deg C |

Table 2 - Input Selection Code

**NOTE:** For linear inputs 00 to 22 decimal point can be positioned after any digit as required by setting the DP parameter.

**For input JUMPER selection refer to table at end of the manual.**

**NORMAL SCALE :** The scale is linear starting at value set for ‘DSPL’ and ending at value set for ‘DSPH’
**CENTRE ZERO SCALE:**  The scale extends on both sides from – ‘DSPH’ to + ‘DSPH’ with ‘DSPL’ at the center.

# ALARM OPTIONS #

The indicator is provided with up to two optional programmable alarms, each alarm is provided with individual setpoint/setpoints and hysteresis.

Alarm LEDs are provided which will glow when the corresponding alarm is active.
Following alarm options can be programmed in normal N/O contact output or reverse N/C contact output.
### High alarm ###
*OPTION 0*   : High alarm , normal N/O contact output

*OPTION 1*   : High alarm , reverse N/C contact output

### Low alarm ###
*OPTION 2*   : Low alarm , normal N/O contact output

*OPTION 3*   : Low alarm , reverse N/C contact output

# OPERATION # 

On power on a self test is done and all LEDs and displays lights up for a few seconds. The indicator then displays the current parameter settings sequentially before starting its normal operation.

#### LIST OF ITEMS DISPLAYED ON POWER ON SELF TEST ####

| Sr. no. | Display | Description |
| ------------- | ------------------| ---------------------------|
| 1. | TIXX | TI is the model and XX is the set input code |
| 2. | Vxxu or VxxF | Where xx is the version number and ‘u’ for universal input or ‘F’ for fixed input |
| 3. | ZZZZ | The set ZERO (DSPL) value for linear inputs (mA,mV & Volts only)  |
| 4. | ssss | The set SPAN (DSPH) value for linear inputs |
| 5. | SQ | ‘Sq’ displayed if square root option enabled for linear inputs |
| 6. | A1xx | If Alarm 1 is available , ‘xx’ indicates alarm 1 type | 
| 7. | dddd | The power ON alarm delay time in seconds if other than 0 |
| 8. | A2xx | If Alarm 2 is available , ‘xx’ indicates alarm 2 type |

Table 3 - Power ON self test items

## OPERATING MENU ##

The indicator is provided with two menus for setpoint entry and configuration. These are as follows:-

**USER MENU** – User menu for entering the alarm setpoints, may be password protected if required or disabled from setup menu.

**SETUP MENU** – This is a password protected menu for configuring the indicator operating parameters.

### PARAMETERS IN SETUP MENU ###

List of parameters that could be programmed in the SETUP menu are:

1. INPUT TYPE – ‘Ip’
2. DISPLAY ZERO -  ‘dSPL’
3. DISPLAY SPAN – ‘dSPh’
4. DECIMAL POINT – ‘dP’
5. SQUARE ROOT EXTRACTION – ‘Sq’
6. ALARM 1 TYPE – ‘A1-t’
7. SENSOR BREAK ALARM 1– ‘A1Sb’
8. ALARM 2 TYPE – ‘A2-t’
9. SENSOR BREAK  ALARM 2– ‘A2Sb’
10. ALARM DELAY FROM POWER ON – ‘AdEL’
11. SETUP PASSWORD – ‘SPAS’
12. USER PASSWORD – ‘uPAS’
13. USER MENU ON/OFF – uMEn’

### PARAMETERS IN USER MENU ###
List of parameters that could be programmed in the USER menu are:

1.	Alarm 1 settings (if provided) 
* Set Value1 – SP1
* Alarm 1 Hysteresis – hy-1

2.	Alarm 2 settings (if provided)
* Set Value2– SP2
* Alarm 2 Hysteresis – hy-2

# INSTALLATION # 

* Check that there is no physical damage to the indicator during transportation.
* Check that the indicator is properly installed in the panel and mounting clamps are properly tightened. 
* Check the power line voltage to ensure that it is within the specified limits.
* Ensure that all input terminal screw is properly tightened.

# POWER CONNECTION #

The indicator is provided with universal AC power supply, any AC supply within the range 90 to 265 V AC can be connected to the power input terminals.
Connect the power supply to the terminal marked ‘L’ Live & ‘N’ Neutral 
**WARNING !!  NEVER  OPEN THE INSTRUMENT COVER WITH THE AC POWER CONNECTED. THIS MAY  LEAD TO  ELECTRICAL SHOCK** 

# SELF TEST ERROR CODES #

During power ON and while running, the systems perform certain self tests to ensure that the indicator does not display a false reading due to system hardware fault. In the process if a hardware fault is detected, the indicator stops normal operation and displays an Error Code.

List of error codes and their meaning is given below: -

| ERROR CODE | REMARKS |
| ------------- | -------------------|
| E1 | Unknown input type selected, select valid type |
| E2 | Calibration error, recalibrate the selected input type |
| E3 |  CJC error, recalibrate thermocouple ambient temperature or hardware failure |
| E4 | ADC error, hardware failure  |

Table 4 - Error codes list

# INDICATOR SPECIFICATIONS #

| Parameter | Explaination|
| ------------------- | ------------------------------ |
| No. of Channels | One |
| System | Advanced microcontroller based |
| Input | Universal mA,mV ,Volts , RTD PT100 , TC As per type selected |
| Input Connection | Rugged Screw type terminal, suitable for wire size ranging 
from 0.2-2.5sq.mm |
| Input Impedance | mA input  < 25 Ohms , Voltage > 100 K  , mV / TC > 1Meg |
| Display | 4 digit 14mm 7seg. Red LED, 
Range –1999 to 9999 |
| Keyboard | Four tactile feedback membrane keys |
| Power Supply | Universal SMPS 95 to 265V AC, 50Hz  or 110 V DC |
| **Enclosure** |
| Mounting Type : | Flush on Panel |
| External Dimension | 48(H) x 96(W) x 129(D) mm |
| Panel Cut-out | 46(H) x 92(W)mm, Depth behind panel: 119mm |

Table 5 - TI 7750 Specifications
























