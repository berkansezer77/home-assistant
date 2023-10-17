_**If you like you can support my work.**_

<a href="https://www.buymeacoffee.com/berkansezer" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a> 

# Spotify Card V3
<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/9a819a43-9cf6-4432-ac2a-9f2297f53cf7" width="350">
<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/57cfe58a-857c-4060-8e16-01cc52177ed0" width="250">
<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/22b5f3d2-5b11-4066-8925-08b509d34aa2" width="200">
<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/437b2d6a-8ab6-4e28-aa8d-81ee23a68ec6" width="150">



# Installation
**How do I install this theme?**

This not a python or anything else coded software but just a code. 

**This is hard because I don't have any code knowledge.**

Don't worry. I have a manual for setup. Everything is explained there and it is super easy to install. 

**Where are the codes ? **

Everything you need including the setup manual is in this page. 🎉

**I don't have the multimedia files you used. ? **

Well they are included as well. Just check below. 🎉
## Page Properties:

- White and Dark Theme Ready.
- 2 different card styles for white and dark template in one single card!!
- Design changes on white theme.
- Switch between white and dark modes with one click
- Beatiful artwork design for every song.
- Room Presence. Start the music in your last entered room (More effective on single occupancy)
- Media Player controls
- Music Follow. Let the music follow you around the house automatically. 
- Hidden playlist. Activate your favorite songs with a single click.
- Exclusively designed for Spotify control.
- Ambilight animations. Glowing light in all over the card.
- Browser Mode integration. 
- Minimalistic design. You can hide spotify playlist. 
- The playing media player is highlighted in a circle.
- Rewind - Forward your music.
- Developed on the basis of Amazon Echo devices but you can also use it with any other media player type.
- Can easily be installed with the given manual

## Before we start, we need some third party tools from Hacs:

- [Swipe card](https://github.com/bramkragten/swipe-card)
- [Card Mod](https://github.com/thomasloven/lovelace-card-mod)
- [Stack in Card](https://github.com/custom-cards/stack-in-card)
- [Mini Media Player](https://github.com/kalkih/mini-media-player)
- [Spotify Playlist Card](https://github.com/custom-cards/spotify-card)
- [Spotcast](https://github.com/fondberg/spotcast )
- [Mushroom Card](https://github.com/piitaya/lovelace-mushroom)

You will also need the Spotify integration to be installed in Home Assistant.
[Link: ](https://www.home-assistant.io/integrations/spotify/)


##Video: 


https://github.com/berkansezer77/home-assistant/assets/84282504/8a183ed1-f587-4924-957d-b3516d63c15c


## Download Multimedia files:


- Files are located at: [Multimedia files](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/spotify-card-v2/media-files.zip)

Page Code: 

- To install the page you need this code: [Page Code](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/spotify-card-v2/page-code)

## Manual:

##Change Theme:

Before we start. To change the theme with a signle click, Browser Mode should be installed and we need to create an input boolean named "input_boolean.theme". Changing the theme from white to dark is quite easy. Just follow the steps. 

1) Download "Google White Theme" from Hacs.
2) Download Mushroom Shadow from Hacs.
3) Register your browser. To do that go to browser mode in side menu and click register this browser.
4) Now we need 2 scripts and 1 automation. After that a single click will change the mode.

[Script White Mode](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/spotify-card-v2/page-code)

[Script Dark Mode](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/spotify-card-v2/theme-google-light-script)

[Automation](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/spotify-card-v2/dark-and-white-mode-automation)

![1](https://github.com/berkansezer77/home-assistant/assets/84282504/25bca020-0ff7-4877-ad45-afb3a27856aa)


Now the boolean we created before(input_boolean.theme) is ready for transformation between themes. The onlu thing you need is you should place tap action into anywhere you like to single click and change the whole theme. 

As shown in above example, changing theme is available with a single click to "Tünaydın" at the upper left corner. The code for that click is: 

```ruby
                tap_action:
                  action: call-service
                  service: input_boolean.toggle
                  target:
                    entity_id: input_boolean.theme
```

##Code Explanation: 

Line 3.

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/3c6445a8-0989-4ba4-83a0-1fe11db49d13)

I used a swipe card here to navigate between my media players. Media Players are starting at line 71 and going until line 418. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/8e8143b8-9754-420d-beeb-428b56dadbfc)

First swipeable section startas at line 21 with an horizontal stack. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/7558e255-81a3-4bf7-9cd0-0791e8cbeb43)

Second swipeable area is at line 243.

Line 435

<img src="[https://github.com/berkansezer77/home-assistant/assets/84282504/437b2d6a-8ab6-4e28-aa8d-81ee23a68ec6](https://github.com/berkansezer77/home-assistant/assets/84282504/1b99596f-83e5-4a05-9d95-d70415eb2d27)" width="150">

I Used a conditional card here. The aim is very simple. This rihanna picture will be shown when nothing is playing on Spotify. On line 456 there is a white solid background circle around rihanna picture. If you like to change the color tone just edit line 457 nad select something different then white. Line 503 and Line 532 also represents :

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/14776086-1d5c-43a0-aea8-a3bcc5545e50)

Spotify and play pictures. Yes Spotify word is a picture here. I used a mushroom chip card and modified it with card mode to place thoese play and spotify pictures under each other. 

Line 561 

Represents the mushroom media player which only appears when spotify is playing anything. Now there is an important point here. On line 596 I used boolean named theme. If any condition named as "('input_boolean.theme', 'on') " it means that white mode is in action. Other words all template will turn into white. So adjustments made for white mode will only work when white mode is active. So volume controls on 602 and and media controls on line 594 acts different on white and dark themes with this conditions.

The magic actually happens here. When in dark mode:

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/2b856e92-0da7-4d86-a105-b387d7974a2e)

The card will look like above picture while on playing state. But If you pass to dark mode the card will transform into :

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/0a879574-907a-4e3c-90ea-9390aa82a9c6)

So 2 different designs for 2 different templates in just one single code. 


Line 678 is for progress bar. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/a8fd894c-b9cd-43c1-a693-3416bded2756)

Line 719 Spotify Card. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/c611370d-64be-4ca3-96f6-26228ba642d2)

I used a conditional card for Spotify card. It only appears when "Playlist" chip is (at the top)single pressed.

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/dfcbc809-ea86-4ff2-abb9-67007fc4b439)

As you can see if the playlist appears on the screen that means 
### Hide - Show Spotify Card:
The first one at line 29 activates Spotify Card at the bottom of the page (code starting from line 610). So I used a conditional card for activating the Spotify - Card. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/ad5e5430-3ee8-4b46-b413-7b53eb7c8d51)

In order for this to work you also have to create an boolean named "input_boolean.modern_dashboard_spotify_Card and place it under playlist options on line 32 as seen on the picture. With this whenever you click "playlist" section the spotify card will appear on the screen. To close it just single click on "Playlist" again.

Line 756

All the little cards I used to create this Spotify Card V2 are inside a "custom:stack-in-card: 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/ed47cae8-4537-49b5-b9dc-7385f9fb8d17)

This stack in card are also modified with card mode starting at line 756. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/c56dc28f-7e95-4747-b208-2f186b282618)

As you can see I have used a conditional structure here with "input_boolean.theme". On line 815 I used a red background which lets the card to look uninterrupted while on dark mode. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/0242e145-2dbc-4257-b563-11ffb346c248)

But when passed to dark mode. The shining lights coming behind the Rihanna picture creates an effect as if it extends beyond the screen in dark mode.

The trick for glowing light behind the Spotify artwork is actually pretty simple. I just used another hidden card floating around the main artwork. So in theory there are 2 artwork here. But one is covered with blur filter on line 770. 

Normally it will look like this: 
![image](https://github.com/berkansezer77/home-assistant/assets/84282504/8ff7ebfc-4e9c-44ed-a641-8ef0e45e8396)

As you can see a second artwork is floating around the main artwork. But when we apply " filter: blur(100px) saturate(200%);" command to line 770 the artwork will transform into a light shadow having the same colors with main album art work. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/ad6d5451-33ef-45cf-bef5-7fc561beb335)

## Room Presence Music:

This card has the capacity to play music on the media player of the room you are in.

This feature is activated with an automation. It is a simple and easy one. What it does is when it is activated through a button the automation checks the sensor and finds out the last room you entered. After that, with a help of an automation it starts to play Spotify music on that rooms media player.

To achieve that we need couple of things things: 

- Spotcast integration to be installed.
- A input Button named "input_button.modern_dashboard_spotify_last_room_music" Create it from helpers section.
- All motion sensors you are going to use has be grouped under helpers > create group >  binary sensor group
- Last Room Motion template sensor (You need at least HA 2023.09 to be installed.
- [Last Room Music Automation](https://github.com/berkansezer77/home-assistant/blob/main/pages/spotify-card-v2/last-room-music-automation)

1) Ceate your button from helpers section of Home Assistant.
2) Go to helpers section again. Choose "Create Helper" and then click "Template". Click "Template a sensor".
Copy and paste this code [Last Motion Sensor](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/spotify-card-v2/room-presence-template-sensor)

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/e66260e6-e1d3-4732-9c4e-dc38a066b76e)

So know our sensor for detecting last motion activated room is ready. 
This sensor will always show you the name of the room where movement was last detected.

3) Now we need the automation. 
[Last Room Music Automation](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/spotify-card-v2/room-presence-automation)

In this automation the important thing to change the name of the media player devices. For example for my office I have an echo device named Office Dot. After that you also have to change the name of the Motion Sensors name to like Ofis Sensör Motion) In my example. 
![image](https://github.com/berkansezer77/home-assistant/assets/84282504/fe636b00-4483-4a1b-b465-bd3a256bf1a9)

So very simple automation 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/923670d2-f1b2-4eb9-9801-4a27a87a67d5)

When you press the button "input_button.modern_dashboard_spotify_last_room_music" The automation will check the status of "sensor.last_motion_activated_sensor" and if it is "Ofis Sensör Motion" the automation will use Spotcast to start music on "Office Dot"(my echo device in that room)

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/e5d086b3-b2f1-4fb1-8249-b7e885e77753)

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/e7811c04-9281-4d79-b5f8-143276052a4a)


Now everything is ready. When we press the play icon on the Play icon the music will automatically start on the last room we entered. Don't forget that we can also start music individually from the topbar media player icons. Just tap any media player icon you want the music to start and it will execute straight away. Double tapping the icon will also stop the media player. 





If you enjoy my work check out my other pojects and please star this page on github. I have many more coming

Enjoy....


