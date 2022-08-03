# Smart-Fireplace

## Idea
To make an old broken fireplace and heater into something a lot better!



## Parts used

- Old Fireplace
- Loewe TV + VESA mounting bracket
- ASUS monitor
- Raspberry Pi4
- Raspberry Pi3
- Wemos D1 mini
- 5V relays X2
- 10M of 12V RGB LED strips
- 500W PC PSU
- My DIY bluetooth smart clock


## Coding
For the Raspberry Pi4 controlling the TV screen I have also got got two relays that control a set of fairy lights and also the WLED D1 mini. These relays are controlled by MQTT using the Mosquito client.
On the TV I mainly play looping VLC files but I also have a "slideshow" that can show art files from various folders, this is controlled via MQTT.

Both Pi's also run a system sesnors script that uses MQTT to report the system health and other sensors like disk space and CPU/RAM usage.

The Pi3 doesnt really have much on it apart from VLC to display the fireplace video files.
It does have a SSH "switch" that sends a command from Home Assistant to turn the HDMI signal off therefore turning off the ASUS monitor.
I tried the same thing on the Pi4 but the TV turns into a bluescreen and will not turn off without a button press on the remote, this is the reason for me building the 
[ESPHome Multisensor](https://github.com/smarthomesnowy/ESPHome-Multisensor) so that I could control the TV via IR.



## Construction
Removing the old fireplace control boards, lighting and heater was pretty easy and left me with a nice glass screen in the front.
I found an old ASUS monitor I do not use anymore and found it to be the perfect size for the hole. I made a shelf on the backside so the monitor just sits on that shelf, I taped the edges of the monitor down to the woodem fireplace surround all the way round to prevent light leakage from the back.

I made another shelf to house the power strip and and the Pi's and relays.

I glued the LED strips all round the backside outside edges of the fireplace and also the TV, I wanted to run the LED strips with ESPHome but found WLED to be a much better fit for the project.


## Conclusion

It was a lot of work but worth every cent and hour spent on this project.
It is a really nice enchancement to the living room and something that money just cannot buy.


