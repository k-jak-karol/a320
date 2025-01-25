# Airbus A320 - Home Cockpit
## Pedestal - Rudder Trim

YouTube Video:
- Part 1: https://www.youtube.com/watch?v=RHGBdZT54NU
- Part 2: https://www.youtube.com/watch?v=LuK0r1u8rrA

[<img src="./preview.png" width="100%">](./preview.png)

### STLs:
- Airbus A320 Rutter Trim Knob-V2 by Mark Ayton: https://www.printables.com/model/438609-airbus-a320-rudder-trim-knob-v2
- Airbus A320 Parking Brake Handle by Mark Ayton: https://www.printables.com/model/436160-airbus-a320-parking-brake-handle

### Parts:
- [DZUS](./../../misc/dzus)

### Hardware:
- [Common hardware](./../../)
- 7-Segment
  - 7-Segment Display with MAX7219 Module: https://amzn.to/4au1awM
  - 7-Segment Display with M1637: https://amzn.to/4hNMCKT
- 1x Round Pushbutton 12mm: https://amzn.to/4a9n1t3
- 90 degree Rotary Switch: https://amzn.to/4hpNkNW
- 3-position 45-degree Rotary Switch: https://amzn.to/4jtrivN
- 7mm ball bearing: https://amzn.to/3Wo7foj

### Scripts
- 7-Segment: `if(# == 0, 8888, if($<0, 'L', 'r') + if(Abs($)<10, ' ', '') + Round(Abs($),1))`

### Arduino pinout
|Type|Name|PIN|Variable|
|-|-|-|-|
|Input|Rudder Trim Reset|2|RUDDER_TRIM_RESET|
|Input|Rudder Left|3|0 (>L:XMLVAR_RUDDERTRIM)|
|Input|Rudder Trim Right|4|2 (>L:XMLVAR_RUDDERTRIM)|
|Input|Parking brake|12|A32NX PED PARK BRAKE ON/OFF|
|Output|Display DIN|6|A32NX Rudder Trim Angle|
|Output|Display CLK|5|A32NX Rudder Trim Angle|
