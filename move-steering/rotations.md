# MoveSteering - rotations

### .rotations(rotations, speed, turn)
Run both motors with a number of degrees the ability to turn.

- `rotations` - number of rotations for the motor to spin
- `speed` - speed at which to run the motors
- `turn` - number between -100 and 100 to denote amount of turning. -100 is maximum left turn. 0 is straight. 100 is maximum right turn.


### Usage
- Move straight forward 1 rotation at 400 speed

```js
var MoveSteering = require('move-steering')

MoveSteering().rotations(1, 400, 0)
```

- Two ways to turn right ~90 degrees

```js
var MoveSteering = require('move-steering')

MoveSteering().rotations(1, 400, 50) // slower turn
MoveSteering().rotations(0.5, 400, 100) // sharper turn
```

- Two ways to turn left ~90 degrees

```js
var MoveSteering = require('move-steering')

MoveSteering().rotations(1, 400, -50) // slower turn
MoveSteering().rotations(0.5, 400, -100) // sharper turn
```
