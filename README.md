Building Apple Homekit-Enabled Environments
-------------------------------------------

# Intro

* I live in Seoul, Korea where has almost none of Apple Homekit devices(except Philips Hue).
* I am maker, so I can build things(almost electronic things) if I needed.
* Then, I find this post: http://adityatannu.com/blog/post/2015/12/13/ESP8266-based-HomeKit-accessories.html

So, I decided to make a Homekit devices with `ESP8266`s and `Raspberry Pi` !

# Item List

## Raspberry Pi

Raspberry Pi 3B (already have).

## ESP8266 boards

I have some `ESP-01`, but with lacks of functionalities, I decided to buy some of other boards. Main consideration is:
* Battery connectivities and rechargeable functionalities. These devices will be placed on top of bookshelf, desks or doors. Battery is the first-class citizen in my mind.
* Arduino compatibility. I am not wary about this for `ESP8266` chips.
* At most `Pinout`s.
* Embedded `USB2Serial` function. It was really hard to connect to USB when using `ESP-01`.

So, I choose Adafruit's `Adafruit FEATHER HUZZAH WITH ESP8266 WIFI`(https://www.adafruit.com/products/2821). It is quietly high price(per $15.95), but has all I want. It has battery connector, built-in charger through USB and maximum pinouts(I thought) by using `ESP-12` module. The `ESP8266 Breakout`(https://www.adafruit.com/product/2471) is one of the nominee for it's price($9.95) but I don't want to struggle with USB and batteries again.

## Batteries

Adafruit has great options for batteries. I just brought 3.7V 2000mA batteries.

## Environmental Sensors

* Temperature/ Humidity:
I already had some experience with SHT-21 sensors. So at this time, I choose `Si7021` sensor for temperature and humidity.

* Luminance: To be determined.

* Noise: `TBD`

# HAP-NodeJS

I forked from `KhaosT`'s repo(https://github.com/KhaosT/HAP-NodeJS). Some changes are made for me:
* Configure bridge's name: `BridgedCore.js`, `15` lines.
* Configure pincode: `BridgedCore.js`, `36` lines.
* `TemperatureHumidity_accessory.js` in the `accessory` directory. This accessory return temperature and humidity at once.

## Supported Services

See this: (HAP-NodeJS-Supported-Services.md)

# Arduino sketch

`TBD`
