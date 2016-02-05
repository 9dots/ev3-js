
# ultrasonic-sensor

to interact with the ev3-js ultrasonic sensor

## Installation

    $ npm install ultrasonic-sensor

## Usage
- basic usage

```js
var UltrasonicSensor = require('ultrasonic-sensor')
UltrasonicSensor(3).inches // => 5.2
UltrasonicSensor(3).cm // 20
```

- usage with [wait](../wait/README.md) and [move-steering](../move-steering/README.md)

```js
var MoveSteering = require('move-steering')
var UltrasonicSensor = require('ultrasonic-sensor')
var wait = require('ev3-js-wait')

MoveSteering().forever(400, 0) // Move straight forever
wait(function () { // hold execution
  return UltrasonicSensor(3).inches <= 10 //until ultrasonic sensor sees an object less than 10 inches away
})
MoveSteering().stop() // Stop the motors
```

## API

### ultrasonicSensor(port)

- `port` -  number of the port that the color sensor is plugged in to.

**Returns:** instance of USSensor

### .inches
Read the number of inches from the ultra-sonic sensor.

### .cm
Read the number of cm from the ultra-sonic sensor.

## License

MIT
