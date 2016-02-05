
# touch-sensor

read information from EV3 touch sensor

## Installation

    $ npm install touch-sensor

## Usage
- basic usage

```js
var TouchSensor = require('touch-sensor')
TouchSensor(3).value // => 0
```
- usage with [wait](../wait/README.md) and [move-steering](../move-steering/README.md)

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
## API

### TouchSensor(port)

- `port` - number of port where the touch sensor is connected

**Returns:** instance of TouchSensor

### .value
Get the value of the touch sensor.

**Returns:** either 0 or 1 to indicate the state of the touch sensor

value | state
---|---
0 | not pressed
1 | pressed
