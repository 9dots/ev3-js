# MoveSteering - forever

### .forever(speed, turn, opts)
Run both motors until they receive a stop command. This is usually used in conjunction with [wait]() and a sensor.

- `speed` - speed at which to run the motors
- `turn` - number between -100 and 100 to denote amount of turning. -100 is maximum left turn. 0 is straight. 100 is maximum right turn.
- `opts` - an object of optional parameters

### Usage

```js
var MoveSteering = require('move-steering')

MoveSteering().forever(400, 0) // Move straight forever
```

- with the [wait](../wait/README.md) function and a sensor

```js
var MoveSteering = require('move-steering')
var TouchSensor = require('touch-sensor')
var wait = require('ev3-js-wait')

MoveSteering().forever(400, 0) // Move straight forever
wait(function () { // hold execution
  return TouchSensor(2).value === 1 //until touch sensor gets pushed
})
MoveSteering().stop() // Stop the motors
```
