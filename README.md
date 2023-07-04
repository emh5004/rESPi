# rESPi
RESTful style API access of GPIO on ESP/RP2040 and Raspberry Pi boards. cURL or python request your way around relays, sensors, and more!

## Background
In the time of plenty, when Raspberry Pis could be had for practically nothing, so many of my projects ran off of a full Linux environment doing really silly basic things. But part of the appeal of this model is because development and prototyping is so simple. Code can be written and tested either directly on the machine with a physical keyboard and mouse or remotely using ssh.
Now this style of tinkering is less of a practical solution for things like simple sensors to detect or trigger things across a house. ESP and RP2040 chips are the way to go for cost and availability, but I find developing for them can be a hassle. This is especially if you're incredibly stingy and want the most bare metal version of the esp8266 so it is tiny and cheap. What I found myself needing/wanting was a way to interface with remote GPIO on some relatively far flung chip and then do any heavier lifting on a central machine. 9 times out of 10, I just want to remotely say to a board to do X on pin Y.

## rESPi: RESTful GPIO access

This project exposes the basic functionality you generally want with GPIO for remote sensing and triggering at logical endpoints reached with http GET requests.
Individual pins can be read, set to be written, set to output PWM, and set to read and send data over i2c all using GET requests. To Do: SPI?
