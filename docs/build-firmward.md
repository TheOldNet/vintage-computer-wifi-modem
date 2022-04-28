Here are the instructions for setting up Arduino.

1) Install Arduino: https://www.arduino.cc/en/software

2) Install the EPS8266 package by going to File -> Preferences and pasting this into the Additional Boards Manager URL

http://arduino.esp8266.com/stable/package_esp8266com_index.json

 

3) Open this esp_modem.ino file:

https://raw.githubusercontent.com/ssshake/vintage-computer-wifi-modem/master/esp_modem/esp_modem.ino

4) Choose your board here and make sure all of the settings in the Tools menu matches this screen shot.

 

5) Change this settings to that everything is erased off the device. By default the config will remain. If the config is corrupted it must be cleared out or else the re-flash won’t help.

 



6) Expand the port menu under Tools and send me a screenshot for my sanity’s sake. I expect to see only one COM port.

 

 

7) Click the upload button to load it onto your device.



8) Upon error the console at the bottom will help. Perhaps copy this and send it to me if you don’t get any further.

 

 

9) The serial port monitor might be helpful here.

 

What’s nice about it is you can quickly change baud rates using the drop down and then issue an “AT” command in the input in the top. If the issue is a serial port mismatch you can burn through the list and try each one.

 

You can also leave it open and set to 300 while you test the resetting by holding the flash button.

One last thing I forgot to mention in the last email, depending on the state of the device it may not be ready for flashing. I have experienced this in the past when I have a bricked device. When you have to do is catch it right at boot which can be tricky or you force it into upload mode.

 

So when you attempt to flash it try these two things because I forget which is the correct one.

1) Hold down flash and press reset

2) Hit upload

3) Let the Arduino program do its thing

 

Or

 

1) Hold down reset

2) Hit upload

3) When the Arduino program says it’s trying to connect/upload release the reset button

The default baud rate for this device when booting and when in flash mode is 74800. So set your serial monitor to that and just observe what happens.

When you hold flash and press reset you should get this.

 

When you just press reset you should get this

 

 

If you see these, these are good signs.

Important, you cannot have this serial monitor open when trying to do the actual flash. It will tie up the port.