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


# Augmented sound walk - Project description

## A sound experimentation on the site of the CHGR and the Bois Perrin in Rennes.

The project "Promenade Sonore Augmentée" (provisional title) is an experimentation around the creation of immersive and geolocalized sound walks in the public space. It brings together 7 partners with complementary skills in content creation, audio technologies and cultural mediation.

## A technical innovation

In order to increase the sound experience of the listeners, we wish to develop a prototype proposing a 3D sound in binaural format and allowing the contents to evolve according to the geographical position of the walker. This sound walk will be able to adapt automatically to the walker's rhythm, without any intervention from the listener, with a system reproducing the functioning of the auditory system, able to determine the distance, the angular position and the direction of the sounds listened to.

The project will attempt to explore the concepts of interactive narration and sound creation in public space. The challenge is to develop a technological solution that is easy to access, does not require any complex equipment, and allows for true immersion.

## Where and when?

The project will be tested in 2021/2022 on the site of Bois Perrin in Rennes and the Centre Hospitalier Guillaume Regnier (CHGR). The Bois Perrin is a remarkable site with many trees, and until now it has been home to the child and adolescent psychiatry departments of the CHGR. We will associate employees and patients of the psychiatric and child psychiatric center Guillaume Regnier, as well as inhabitants willing to participate in this sound creation.

## 7 partners

Supported by Ars Nomadis, this project also associates 6 other partners to develop an adapted digital solution and to think about new uses in terms of communication and mediation:

* Noise Makers, a Rennes-based company specialized in 3D audio technologies.
* EUR-CAPS, University School of Research - Creative Approaches to Public Space.
* Digital Campus Rennes, Web and Digital school
* ESRA, School of Audiovisual Production.
* IRISA-CNRS, Institute of Research in Computer Science and Random Systems, PANAMA laboratory.
* Marine Frugès, graphic design.
