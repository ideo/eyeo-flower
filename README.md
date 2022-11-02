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

[Online tool for petal shape generation](https://observablehq.com/@jftesser/eyeo-flower)

For the petal material we use [translucent Yupo:](https://www.amazon.com/dp/B004XC7CE8?psc=1&ref=ppx_yo2ov_dt_b_product_details)

Cut on a Cricut machine with the setting "Light Cardstock - 65lb - 176GSM"

<h2>Parts and Assembly</h2>
The gerber, CPL and BOM files are formatted for PCB and assembly services from JLCPCB. So you should be able to just send them the boards.  Last time I sent them out, I had to rework the TPS63070 (not sure why) and JLCPCB had a few issues with part placement packing around that area.  I hand assembled a few of the parts they wouldn't do, and hot-air reworked some of the TPS63070 chips and the boards worked fine.<br />

[The gooseneck USB cables](https://metaltube.en.alibaba.com/product/1600324362930-827664414/Fast_Charging_Phone_Cable_2_4A_USB_Lighting_Type_C_Micro_USB_with_Adjustable_Flexible_Gooseneck_Arm_Phone_Stand_Holder.html?spm=a2700.shop_index.111720.2.137c2221o8sztU) Make sure to select the USB C option!

[The nitinol wire we used](https://musclewires-com.3dcartstores.com/Muscle-Wiresreg-Actuator-Wire-100-%C2%B5m-LT-5-meter-_p_216.html)

8x [KF2-M3-ET Broaching Nuts](https://www.dbroberts.com/pemkf2-m3.html?&utm_source=octopart&utm_medium=buy) need to pe pressed into the holes on the board. I have a lathe at home so I used this to make a tool for a mini arbor press to press them in, but there are likely other ways to achieve a good press-fit.

We used 8x of these ["Cheese Head M3 Screws"](https://www.mcmaster.com/91800A113/) in the broaching nuts. They are narrower than the nuts, so they won't contact each other, they also have a nice flat bottom surface to ensure connection with the nitinol.

You will need some standard thru hole resistors to limit the current the goes to the wire. With our petal shape we end up with about 13cm of wire going from post to post. Our wire has 126Ω/m resistance and rated current maximum of 200mA. So our wire is 126⋅0.13 = 16.38Ω. To calculate the resistance we want at 5V max voltage, we use Ohm’s law to get V/I = R, 5/0.2=25Ω. We selected 10Ω resistors to put in series with the wire to make sure we never deliver too much current to the wire. 

[The pogo pins we used for our board programmer jig are these](https://www.amazon.com/gp/product/B08CD7FNK8)
