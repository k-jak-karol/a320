# Airbus A320 - Home Cockpit
## Pedestal - Cockpit Door Panel

YouTube Video: https://www.youtube.com/watch?v=UO_dVJxS8eo

[<img src="./preview.png" width="100%">](./preview.png)

### Parts:
- [Announciator](./../../misc/announciator)
- [DZUS](./../../misc/dzus)

### Hardware:
- [Common hardware](./../../)
- 1x Momentary switch (On)-Off-(On): https://amzn.to/4h9SfT5
- 1x Round Pushbutton 12mm: https://amzn.to/4a9n1t3

### Scripts
- Cockpit Door Open LED: `if(# == 0, 255, if($ == 1, if(# == 2, 64, 255),0))`
- Cockpit Door Fault LED: `if(# == 0, 255, 0)`
