# dark_melty
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


## Accelerometer New:
- Needs to measure high G forces (1500rpm at 6cm is 150G) - see centrifuge calculator
- Sparkfun's pre-mounted ADXL193 is the currently recommended solution (obsoleted ) bought a EVAL-ADXL375
- Freescale 200g MMA2301Eg - used extensively in the past (needs SOIC 16 mount / may not be available)


## Some kind of motor(s) / wheel(s)
- Project works fine with either 1 or 2 motors
- Hard rubber doesn't work that well
- Foam wheels seem to work best (see wheel comparison video)

## A heading LED (change this to text flashing status..)
- I want to add a POV (persistants of vision shape/text on the bot)



## Brushless Motor / Controller Option:
used one form finger tech


