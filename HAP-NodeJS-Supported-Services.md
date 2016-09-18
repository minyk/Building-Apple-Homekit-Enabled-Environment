# Services

This list is for my own needs. See full list in the `HAP-NodeJS`'s `lib/gen/HomeKitTypes.js`

## AccessoryInformation

For adding some info about accessory:
``` javascript
var light = exports.accessory = new Accessory('Light', lightUUID);
light
  .getService(Service.AccessoryInformation)
  .setCharacteristic(Characteristic.Manufacturer, "Oltica")
  .setCharacteristic(Characteristic.Model, "Rev-1")
  .setCharacteristic(Characteristic.SerialNumber, "A1S2NASF88EW");
```

* Some options for firmware versions, etc.

## BatteryService

For battery managements. This would be useful for battery backed devices. It requires:
* Characteristic.BatteryLevel: 0 - 100, min step 1.
* Characteristic.ChargingState: 0(not charging), 1(charging)
* Characteristic.StatusLowBattery: 0(normal), 1(low level battery)

## HumiditySensor

For humidity level:
* Characteristic.CurrentRelativeHumidity: 0 - 100, percentile, min step 1.

Options:
* Characteristic.StatusLowBattery: 0(normal), 1(low level battery)
* Characteristic.StatusActive: boolean.
* Characteristic.Name

## LightSensor

* Characteristic.CurrentAmbientLightLevel: 0.0001 - 100000, min step 0.0001, `LUX`

Options:
* Characteristic.StatusLowBattery: 0(normal), 1(low level battery)
* Characteristic.StatusActive: boolean.
* Characteristic.Name

## MotionSensor
## OccupancySensor
## Outlet
## SmokeSensor
## StatefulProgrammableSwitch
## StatelessProgrammableSwitch
## Switch

## TemperatureSensor

For Temperature:
* Characteristic.CurrentTemperature: 0 - 100, min step 0.1, `CELSIUS`

Options:
* Characteristic.StatusLowBattery: 0(normal), 1(low level battery)
* Characteristic.StatusActive: boolean.
* Characteristic.Name
