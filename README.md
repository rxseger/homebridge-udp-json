# homebridge-udp-json

UDP server for receiving JSON messages from remote sensors on your network,
plugin for [Homebridge](https://github.com/nfarina/homebridge)

## Installation
1.	Install Homebridge using `npm install -g homebridge`
2.	Install this plugin `npm install -g homebridge-udp-json`
3.	Update your configuration file - see below for an example

## Configuration
* `accessory`: "UDPJSON"
* `name`: descriptive name
* `name_temperature` (optional): descriptive name for the temperature sensor
* `name_humidity` (optional): descriptive name for the humidity sensor
* `listen_port` (8268): UDP port to listen for packets on

This currently plugin creates two services: TemperatureSensor and HumiditySensor,
but other sensors

UDP packets are expected to be sent from a remote sensor in JSON, for example:

```json
{"temperature_c": 24.35, "pressure_hPa": 1010.73, "altitude_m": 21.01, "humidity_percent": 38.20}
```

This is a custom structure, but simple enough to send from cheap Wi-Fi enabled microcontrollers
such as the ESP8266.

## See also

* [homebridge-bme280](https://www.npmjs.com/package/homebridge-bme280)
* [homebridge-udp-lightsensor](https://www.npmjs.com/package/homebridge-udp-lightsensor)
* [homebridge-udp-contactsensor](https://www.npmjs.com/package/homebridge-udp-contactsensor)
* [homebridge-udp-lock](https://www.npmjs.com/package/homebridge-udp-lock)
* [homebridge-blinds-udp](https://www.npmjs.com/package/homebridge-blinds-udp)
* [homebridge-udp-multiswitch](https://www.npmjs.com/package/homebridge-udp-multiswitch)

## License

MIT
