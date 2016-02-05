# MoveSteering - degrees

### .degrees(degrees, speed, turn)
Run both motors for a number of degrees with the ability to turn.

- `degrees` - number of degrees for the motor to spin
- `speed` - speed at which to run the motors
- `turn` - number between -100 and 100 to denote amount of turning. -100 is maximum left turn. 0 is straight. 100 is maximum right turn.

### Examples
```js
var MoveSteering = require('move-steering')

MoveSteering().degrees(90, 400, 0) // move the motor 1 quarter turn
MoveSteering().degrees(180, 400, 100) // move the motor 1/2 turn and turn right
```
