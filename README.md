DHT11
=====

An Arduino library for reading the DHT11 sensor of temperature and humidity.

Written by Mark Ruys, <mark@paracas.nl>.

Features
--------
  - Support for DHT11 only
  - Low memory footprint
  - Very small code

Usage
-----

```
#include "DHT11.h"

DHT11 dht;

void setup()
{
  Serial.begin(9600);

  dht.setup(2); // data pin 2
}

void loop()
{
  delay(dht.getMinimumSamplingPeriod());

  Serial.print(dht.getHumidity());
  Serial.print("\t");
  Serial.print(dht.getTemperature());
}
```

Installation
------------

Place the [DHT11][download] folder in your `<arduinosketchfolder>/libraries/` folder (Usually c:\Users\YourUser\Documents\Arduino\libraries).
You may need to create the `libraries` subfolder if its your first library. Restart the Arduino IDE. 

[download]: https://github.com/MarcosMeli/DHT11/archive/master.zip "Download DHT library"
