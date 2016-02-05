# MoveSteering - timed

### .timed(time, speed, turn)
Run both motor for a specified amount of time.

  - `time` - time in milliseconds
  - `speed` - speed at which to run the motors
  - `turn` - number between -100 and 100 to denote amount of turning. -100 is maximum left turn. 0 is straight. 100 is maximum right turn.

### Usage

```js
var MoveSteering = require('move-steering')

MoveSteering().timed(2000, 400, 0) // Move straight for 2 seconds
MoveSteering().timed(1000, 400 -100) // Turn left for 1 second
```
