# eyeo-flower
Custom SAMD21E17D Arduino compatible board for making kinetic flora

<h2>To set up your Arduino Environment:</h2>

Go to Arduino → Preferences → Additional Board URLs
Add these to your Additional Boards Manager URLs
https://adafruit.github.io/arduino-board-index/package_adafruit_index.json
https://raw.githubusercontent.com/ideo/ArduinoCore-samd/eyeo-flower/package_ideo_index.json

Go to Tools → Board → Boards Manager
Type “samd” and install Adafruit SAMD (will take some time) and IDEO SAMD Boards

Select Tools → Manage Libraries 
Search and install Adafruit Zero FFT Library

Select Tools → Board → IDEO SAMD → Eyeo Flower
Select correct Port in Tools → Port (“/dev/cu.usbmodem…” on OSX)

<h2>To make your own custom flower shape:</h2>
https://observablehq.com/@jftesser/eyeo-flower

For the petal material we use [translucent Yupo:](https://www.amazon.com/dp/B004XC7CE8?psc=1&ref=ppx_yo2ov_dt_b_product_details)

Cut on a Cricut machine with the setting "Light Cardstock - 65lb - 176GSM"
