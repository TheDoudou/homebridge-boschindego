# homebridge-boschindego

View and manage Bosch Indego Mower.

It's work :

    - Auth
    - Read state
	- Add switch for mowing or docking

And don't work :

    - Remake the code (https://github.com/nfarina/homebridge/blob/master/example-plugins/homebridge-samplePlatform/index.js)
    - Add function with the Bosch API (https://github.com/zazaz-de/iot-device-bosch-indego-controller/blob/master/PROTOCOL.md)

# Installation

1. Install homebridge using: `npm install -g homebridge`
2. Install this plugin using: `npm install -g homebridge-boschindego`
3. Update your configuration file. See sample-config.json in this repository for a sample.

# Configuration

The available fields in the config.json file are:
 - `accessory` Accessory value.
 - `name` Accessory name.
 - `model` Additional information for the accessory.
 - `email` and `pass` fields used to authenticate the request into the device.
 - `update_interval` If not zero, the field defines the polling period in miliseconds for the sensor state. When the value is zero, the state is only updated when homebridge requests the current value.
 - `view_log` Set true for watch plugin log.

Example:

 ```
 "accessories": [
     {
        "accessory": "BoschIndego",
        "name": "Mower",
		"model": 1000,
        "email": "test@test.com",
		"pass": "test",
		"update_interval": "10000",
		"view_log": false
     }
 ]

```
