# Info  
[![Build Status](https://travis-ci.org/vadrian89/cumulus-qt.svg?branch=master)](https://travis-ci.org/vadrian89/cumulus-qt)   
Both offline and online installers for 64 bit Linux distributions can be found at the [releases page](https://github.com/vadrian89/cumulus-qt/releases).
Still not decided on 32 bit.

For any feedback you can mail me at verbanady@gmail.com, please add the following subject so I can save them into a special category: Cumulus - Feedback.
Thanks!

# Cumulus

Full port Qt/Qml is here!

Simple weather application, powered by [Yahoo! Weather](http://weather.yahoo.com) & [Open Weather Map](http://openweathermap.org/)

Forked from [typhoon](https://github.com/apandada1/typhoon) which was
Based on [Stormcloud](https://github.com/consindo/stormcloud/) by [Jono Cooper](https://twitter.com/consindo).

Features:
- resizable window with weather data adjusting accordingly
- units recalculations on-the-fly without data needed to be re-downloaded
- colors selectors for background and text with alpha channel, knock yourselves up ^^
- tray icon, with aditional data to be added on menu :)
- qt installer, without root installation to allow future updates fast without breaking on upgrade
- possbility for multiple instances with different settings and locations

# For multiple instances:

1. make a new shell script with the following content updated for Cumulus installation path  
#!/bin/bash  
\<path-to-cumulus-executable> -i \<whatever-you-want>

Example: /home/user/Cumulus/Cumulus -i NewInstance

2. make the shell script executable

# In case you want to build it yourself:

- recommended Qt version: 5.8
- remove the following line from Cumulus.pro file: QMAKE_LFLAGS += "-Wl,-rpath,'$$ORIGIN/lib'"
- remove the following entry from qml.qrc file: "qt/etc/qt.conf"

# Major Thanks
- [Daryl Bennett](https://github.com/kd8bny)
- [Archisman Panigrahi](https://github.com/apandada1)
- [Erik Flowers](https://github.com/erikflowers) for his [weather icons](https://github.com/erikflowers/weather-icons),
which sadly has discontinued support for them

# Known Issues
- The resizing is implemented, but it's a bit haotic on Linux-based OSes, looking into it and hopefully I will find a solution soon.

# TODO
- Add another API
- Code refactoring
- Improve application resizing

