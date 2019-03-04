# Arduino CAN

[![Build Status](https://travis-ci.org/nzottmann/arduino-CAN.svg?branch=master)](https://travis-ci.org/nzottmann/arduino-CAN)

A Particle library for sending and receiving data using CAN bus with MCP2515.
Based on https://github.com/sandeepmistry/arduino-CAN, with small changes to be compatible to Particle.

The library is only tested with the mesh modules Argon, Boron and Xenon. Older generations have an on-chip CAN controller.

## Compatible Hardware

* [Microchip MCP2515](http://www.microchip.com/wwwproducts/en/en010406) based boards/shields

### Microchip MCP2515 wiring

| Microchip MCP2515 | Particle |
| :---------------: | :-----: |
| VCC | 5V |
| GND | GND |
| SCK | SCK |
| SO | MISO |
| SI | MOSI |
| CS | 10 |
| INT | 2 |


`CS` and `INT` pins can be changed by using `CAN.setPins(cs, irq)`. `INT` pin is optional, it is only needed for receive callback mode. If `INT` pin is used, it **must** be interrupt capable via [`attachInterrupt(...)`](https://www.arduino.cc/en/Reference/AttachInterrupt).


## API

See [API.md](API.md).

## Examples

See [examples](examples) folder.

## License

This library is [licensed](LICENSE) under the [MIT Licence](http://en.wikipedia.org/wiki/MIT_License).
