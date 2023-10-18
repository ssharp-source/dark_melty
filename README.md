# dark_openmelt
open source melty brain - info at nothinglabs.com

Fork to mood drive, filtering and explore differnet HW targets

Goal to have a fork donen by the end of sept(that didnt happen). to test by the early..late part of Oct

If this turns into a massive rewrite the I might make a seperate repo and release it (it happend and Im nerfing this to arduino)

Whats differnet (I think)
-IF two wheels use them continuously (not just 180 to 350 degree) but "foward" bottome wheel positve from 180 to 0 and top wheel negative direction from 0 to 180. this should make a two wheeled version suuuuper fast
- Fir filter the IMU
- Add external frame refernece (may be a bridge too far)
- target bluepill


## Hardware List (major items)
### MCU Board:
- #### goal: "blue pill" stem32 (using ardino IDE/loader) 
- backup plan Atmel 328 boards should work - however may require additional hardware / code changes


## Accelerometer:
- Needs to measure high G forces (1500rpm at 6cm is 150G) - see centrifuge calculator
- Sparkfun's pre-mounted ADXL193 is the currently recommended solution (obsoleted ) bought a EVAL-ADXL375
- Freescale 200g MMA2301Eg - used extensively in the past (needs SOIC 16 mount / may not be available)


## Some kind of motor(s) / wheel(s)
- Project works fine with either 1 or 2 motors
- Hard rubber doesn't work that well
- Foam wheels seem to work best (see wheel comparison video)

## A heading LED (might change this to text flashing status..)
- Use the correct size limiting resistor
- Be careful not to overload your voltage regulator or the Orangutan's motor controller

## Brushless Motor / Controller Option:
- Open Melt now supports brushless motors / controllers via high update rate PWM
- Any brushless motor controller supporting input PWM frequencies over 305 hz should work (although this specification is usually not listed)
- Testing was specifically done with a Hobbywing Pentium-18a
- Openpilot.org lists other ESCs that support high refresh rates which will likely work (but haven't been tested)
- All wiring is the same - except that motor control pins (PD2 and PD4) are connected directly to the signal pin of the ESC


