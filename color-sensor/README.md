
# color-sensor

read information from the ev3 color sensor

## Installation

    $ npm install color-sensor

## Usage
- basic usage

```js
var ColorSensor = require('color-sensor')
ColorSensor(1).reflected // => 88
ColorSensor(1).color // => 7
```

- usage for a basic line follow

```js
var MoveSteering = require('move-steering')
var ColorSensor = require('color-sensor')

while (true) { // infinite loop
      var brightness = ColorSensor(1).reflected // get the reflect light intensity
      if (brightness >= 50) { // if it is bright
        MoveSteering().forever(250, 30) // turn right
      } else { //otherwise
        MoveSteering().forever(250, -30) // turn left
      }
}
```

## API

### ColorSensor(port)

- `port` - number of the port that the color sensor is plugged in to.

**Returns:** instance of ColorSensor

### .reflected
Gets the value of the reflected light intensity.

**Returns:** number between 0 and 100

### .color
Gets the value of the color.

**Returns:** color value between 0 and 7

number | color
---|---
0 | no color
1 | black
2 | blue
3 | green
4 | yellow
5 | red
6 | white
7 | brown

## License

MIT
