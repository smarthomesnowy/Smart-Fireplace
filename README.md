# Smart-Fireplace

## Idea
To make an old broken fireplace and heater into something a lot better!
What I have ended up with is a screen in the fireplace that shows a video of a fireplace in 720p (or any other video file) a TV on the wall that shows all kinds of "art" videos and "art" slideshows. The whole thing is covered in RGB LED strips that can do hundreds of different effects and even be "sound reactive" so the effects and colours change in time to music being played.

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
- [My DIY bluetooth smart clock](https://github.com/smarthomesnowy/ESPHome-BluetoothClock)



## Coding
For the Raspberry Pi4 controlling the TV screen I have also got got two relays that control a set of fairy lights and also the WLED D1 mini. These relays are controlled by MQTT using the Mosquito client.
On the TV I mainly play looping VLC files but I also have a "slideshow" that can show art files from various folders, this is controlled via MQTT.
[The DIY bluetooth smart clock](https://github.com/smarthomesnowy/ESPHome-BluetoothClock) that sits ontop of the fireplace is bluetooth paired to the Pi4 and the Pi4 is running MDP media server so that it can be a mnedia player device within Home Assistant. This then allows me to play TTS ( like google assistant or Alexa) messages and play mp3 "alert" files.

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

The fireplace was broken and was going to be thrown out so I got that for free, The TV was thrown out in the trash outside my apartment, the PC PSU was in a PC thrown out in the street, the ASUS monitor is over ten years old and has sat doing nothing for about 5 years. I own 5 different Pi of all flavours and had the Pi4 and Pi3 sitting around doing nothing so I was happy to use them for this project.

So all in all this was a recycling project - making something really nice out of thrown away or unused things.