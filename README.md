fork of adafruit sht31 to allow passing in an initialised wire pointer so can use non standard pins on esp8266
requires the modified 

https://github.com/pwr33/Adafruit_BusIO

for the mods to the I2CDevice class

Basically problem arose because a chinese clone sensor board (sgp30) had labelled up sda/scl wrong way round on the silk screen (Doh!), so I wired up some stripboard incorrectly and to get it to work for testing purposes needed to do Wire.begin(5,4) (where default is (4,5))

obviously now I have proved that is what it was I do not need it anymore after I rewire this stripboard and wire up the rest of the test ones correctly.

However this will be useful if you want to use this library on an esp-01 that only has gpio 0 and 2 broken out to pins.
