# ArsNomadis-Player

Ars Nomadis Player is a code for a geolocated audio player.

Parsing and scanning of a .json file for implementation on the microcontroller via an SD-card.

The audio zones can be programmed on the official [ArsNomadis-Editor](https://arsnomadis-editor.vercel.app/) page.


## Hardware

For this project we're using a teensy 4.0 which can be found [here](https://www.pjrc.com/store/teensy40.html), an [audio shield](https://www.pjrc.com/store/teensy3_audio.html) and the [Neo 6MV2](https://letmeknow.fr/fr/mouvements-et-positions/1247-module-gps-3007591023705.html) gps module.

The Teensy microcontroller :
![Teensy](https://www.pjrc.com/store/teensy40_front.jpg)

The specific audio shield :
![audio shield](https://www.pjrc.com/store/teensy3_audio.jpg)

## Installation

First of all you have to install the Teensyduino plugin, so you will be able to use the Arduino IDE to program the Teensy.

Everything concerning the Teensyduino installation is explained on the [official PJRC website](https://www.pjrc.com/teensy/td_download.html).


## Usage

Then we are using several libraries, but the main libraries are these ones :

```c
#include <TinyGPS++.h>
```
For the GPS module.

The main library that uses audio files with the shield is preinstalled by Teensyduino.
```c
#include <Audio.h>
```

For the scanning of the SD-card you will have to install these libraries, it will be useful for the reading of the .json file provided by the ArsNomadis-Editor.

```c
#include <LinkedList.h>
#include <ArduinoJson.h>
```

Finally, an important audio library alternative is this one, it can be found on [GitHub](https://github.com/FrankBoesing/Teensy-WavePlayer).

```c
#include <play_wav.h>
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[Ars Nomadis](https://www.arsnomadis.eu/)
