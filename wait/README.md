# wait

wait block for use with running the motor forever

## Installation

    $ npm install ev3-js-wait

## Usage

```js
var wait = require('ev3-js-wait')
var TouchSensor = require('touch-sensor')
var MoveSteering = require('move-steering')

// Move forever
MoveSteering().forever(300)

// Wait for the touch sensor to activate
wait(function () {
  return TouchSensor(3).value === 1
})

// Turn the robot to the right
MoveSteering().degrees(360, 300, 100)
```

## API

### wait(fn)

- `fn` - function that returns a conditional

## License

MIT
