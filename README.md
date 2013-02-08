# RPi_RFM12B_ISP

RFM12B and Atmel ISP programmer shield for Raspberry Pi


## Avrdude

Use the patched version of avrdude from http://project-downloads.drogon.net/files/. I suggest copying the
.avrduderc file from the avrdude directory in this repository to your home directory. It will create create 
the correct definitions for two new programmers, gpio0 for the onboard microcontroller and gpio1 for programming
other microcontrollers.


## Using the Arduino IDE

If you do not have a <code>hardware</code> directory inside your Arduino <code>sketchbook</code> folder
then create one. Copy the raspi directory and its entire contents to the hardware directory. Restart the 
Arduino IDE. You should now have two new board options, <code>ATmega328 @ 8MHz on RasPi</code> and 
<code>ATmega328P @ 8MHz on RasPi</code>. Select the one which matches the microcontroller. There are also two new
programmers; <code>Raspberry Pi GPIO (onboard)</code> and <code>Raspberry Pi GPIO (external ISP)</code>. 
The onboard one will be used automatically to upload new sketches to the RFM12B/ISP shield. The external ISP
programmer can be selected to program other microcontrollers from within the Arduino IDE.

## License

Hardware is released under the Creative Commons Attribution-ShareAlike
3.0 Unported (CC BY-SA 3.0)
http://creativecommons.org/licenses/by-sa/3.0/

Software is released under the GNU Lesser General Public License,
version 2.1. 
http://www.gnu.org/licenses/lgpl-2.1.html
