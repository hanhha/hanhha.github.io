---
title: Be a foolish newbie again
published: true
---

Recently days I had an idea about a small box that collect data about temperature and humidity inside my car, then talk to Android HUD via bluetooth to show those informations in a widget. I tried with DHT11 sensor, HC-06 bluetooth module and a spare Arduino 2560 board. Everything was fine, except that my Android terminal can not send anything to the system of HC-06 and Arduino board. I though that could be a fault of HC-06.

Then I decided to move whole system to an Attiny13a MCU. Wow, I stuck right at the first step - had no programmer to flash MCU. I had did program MCU before with a Raspberry Pi board, but now that board had another duty and I didn't want to interrupt him. I opted to use my Mega board as an AVRISP. Uploading Arduino ISP example, connecting pins, using **Avrdude** to flash to Attiny13a via Mega, all I got was error (so shame that I forgot detail error report completely). I had tried any advises I got from Internet without any luck.

Finally, thinking that I would have to program the MCU many times, not only for this project, I bought an **USBasp v2.0** programmer from a local store because of the cheapest price. Some stores sold USBasp, some sold USBasp v2.0, and all of them described that can use with Avrdude. Well, I got what I paid for. It doesn't work.

Luckily, not only me got this problem. Some kind guys figured out a way to hack that programmer to work like a original one. There was not other choice, I had to disrupt my Raspberry Pi board to turn it to a AVR programmer again. Using it to flash a modified firmware to bought programmer board to make it compatible with Avrdude, then try again. Now everything worked.
