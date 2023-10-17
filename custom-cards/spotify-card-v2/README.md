_**If you like you can support my work.**_

<a href="https://www.buymeacoffee.com/berkansezer" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a> 

<img src="https://user-images.githubusercontent.com/84282504/226495334-d192e575-a72f-4218-a733-9d0714e11a46.png" width="450">
<img src="https://user-images.githubusercontent.com/84282504/226495337-b787bd17-de30-48cf-a60b-0829c90062e1.png" width="350">



https://github.com/berkansezer77/home-assistant/assets/84282504/748c00e9-644d-40f9-98ab-cc1a5c24a18b


# Installation
**How do I install this theme?**

This not a python or anything else coded software but just a code. 

**This is hard because I don't have any code knowledge.**

Don't worry. I have a manual for setup. Everything is explained there and it is super easy to install. 

**Where are the codes ? **

Everything you need is in this wiki page. 🎉

**I don't have the multimedia files you used. ? **

Well they are included as well. Just check below. 🎉
## Page Properties:

- Room Presence. Start the music in your last entered room
- Media Player controls
- Music Follow. Let the music follow you around the house automatically. 
- Spotify Card integrated. Start your playlist from the card.
- Exclusively designed for Spotify control.
- Ambilight animations.
- Browser Mode integration. 
- Minimalistic design. You can hide media players and spotify playlist. 
- See which media player is currentlu playing
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


## Screenshots: 

<img src="https://user-images.githubusercontent.com/84282504/226496244-d3505e0e-7c88-46b0-aa0d-1681512bb89c.gif" width="250">
<img src="https://user-images.githubusercontent.com/84282504/226495338-6b36471c-b58d-4911-8d5b-d1ba5b5aa70a.png" width="250">
<img src="https://user-images.githubusercontent.com/84282504/226581606-1c9a2ec3-d4ae-4171-9b5d-89b61d33fc64.gif" width="250">



## Download Multimedia files:


- Files are located at: [Multimedia files](https://github.com/berkansezer77/home-assistant/blob/main/pages/spotify-card-v2/spotify-card.zip)

Page Code: 

- To install the page you need this code: [Page Code](https://github.com/berkansezer77/home-assistant/blob/main/pages/spotify-card-v2/page-code)

## Manual:

Okay this is a minimalist Spotify Card. Let's start with code explanation and go line by line. 

Line 3. 

![image](https://user-images.githubusercontent.com/84282504/226582419-2260de02-d415-4849-af84-77829f65b571.png)

I used a swipe card here to navigate between my media players. Media Players are starting at line 29 and going until line 336. 

### Hide - Show Spotify Card:
The first one at line 29 activates Spotify Card at the bottom of the page (code starting from line 610). So I used a conditional card for activating the Spotify - Card. 

<img src="https://user-images.githubusercontent.com/84282504/226583621-412ce6da-f19c-4f49-9c8e-c3dcbadb2980.png" width="250">

The name of the boolean for displaying the Spotify Card is "input_boolean.modern_dashboard_spotify_card". 

![image](https://user-images.githubusercontent.com/84282504/226584613-04be095a-3d2b-4126-b78c-eced460ed91e.png)

As you can see when you tap the playlist chip once it activates the Spotify card. If you tap it again it hides the card. 

![image](https://user-images.githubusercontent.com/84282504/226586064-1c8f7e11-a423-49ed-8f0b-069e767045e3.png)

The conditional card is used here with the boolean I created. 

### Hide - Show Media Players:
There is also another tapping feature in this "Playlist chip"

![image](https://user-images.githubusercontent.com/84282504/226586435-40cc0891-625c-4d66-812e-27330b7a6bff.png)

In line 46 I created another boolean named "input_boolean.modern_dashboard_spotify_card_hide_media_players". This helps the chip to display a double tap feature. When you tap it twice it hides all the media players at the top bar. 

<img src="https://user-images.githubusercontent.com/84282504/226586758-ae2ad4f3-f9dd-46dd-9fea-a4321edda7e5.png" width="250">
<img src="https://user-images.githubusercontent.com/84282504/226586816-c55896eb-7e9b-49ec-8787-5fc86494acb3.png" width="250">

To reactivate the media player chips just click song name twice.

![image](https://user-images.githubusercontent.com/84282504/226589668-f3a8f1f9-ba97-4bf3-933c-a0b3cf3cfe92.png)
 
![gif4](https://user-images.githubusercontent.com/84282504/226589408-6e3ba928-2256-45cd-b11e-b8abb44c8acc.gif)

### Media Player Chips: 

Media player Chip codes are starting from line 66. They all have some basic features. If you have "Spotcast" service installed from hacs, you can start a music straight away with the clicked media player. 

  
![image](https://user-images.githubusercontent.com/84282504/226591154-c96d0c5f-7eee-483e-810b-5b6d56e1c34e.png)

In line 77 a single tap action starts music on my Echo dot at living room(salon). A force start feature is also implemented.

![image](https://user-images.githubusercontent.com/84282504/226591570-d123b51c-8904-4895-b2f7-b08a57bf7d42.png)

A double tap also stops the media player from playing the music. 

With the card mod I also added some css styles. 

![image](https://user-images.githubusercontent.com/84282504/226591843-20b8e66d-e364-42d0-907b-64e1e1099971.png)

In line 98 the css code lets the media player chip to feature a box shadow and changes inner color to black if its status is currently "playing". 

![image](https://user-images.githubusercontent.com/84282504/226592120-57f1fd7e-28ef-4f9d-b43d-2f5b748df173.png)

## Spotify Cover:

If there is nothing currently playing a welcome screen will activate. 

<img src="https://user-images.githubusercontent.com/84282504/226495334-d192e575-a72f-4218-a733-9d0714e11a46.png" width="250">

The codes for this screen starts from line 337.

There is one important conditional card rule here. To let the page understand that spotify card is not playing anything we have to create a boolean and use an automation for that. The boolean I used is named "input_boolean.modern_dashboard_spotify_card_update_spotify_status". This boolean is only activated when Spotify is in "Paused" or "Playing" status. When it is at "idle", "unalable" or "standby" the boolean turns off. 

When the boolean is on(meaning spotify is on paused or playing) the welcome screen shown above will disappear and media player screen will show on the page. 

<img src="https://user-images.githubusercontent.com/84282504/226594628-3762610d-3ca2-4cc3-a43e-6035834999d2.png" width="250">

Just create this automation. Link is below.

[Spotify Status Update Automation](https://github.com/berkansezer77/home-assistant/blob/main/pages/spotify-card-v2/spotify-update-automation)

### One little note: 

This automation lets the boolean to track spotify status. But sometimes Spotify will not not update it straight away. Sometimes it might be laggy. If you run into any trouble like this just create another automation to force Spotify update its status in every 3 seconds. Link is below for this automation 

[Force Spotify to update it's status](https://github.com/berkansezer77/home-assistant/blob/main/pages/spotify-card-v2/force-spotify-to-update-status)

## Welcome Screen background animation:

I used a welcome screen background animation. Css code for this animation starts from line 355. The basics of this css is quite simple actually. It creates a blurred image behind the real image and animates according to it. To see that clearly just go to line  364 and change "blur(100)px" to "blur(10)px". You shall now see the shadow of the behind picture very clearly. 

<img src="https://user-images.githubusercontent.com/84282504/226613510-fafce709-04a3-4f7f-811f-f1a4a2f5b5fd.png" width="250">
<img src="https://user-images.githubusercontent.com/84282504/226613930-7e790d01-862b-4e12-878a-6d9400a946fb.png" width="250">

It can be seen very clearly from the above pictures. When we minimize the effect the background picture can easily be seen. But with the 100 blur it transforms into a light show. In my instance the backrground picture is "background: url('/local/png/red.jpg') " on line 362. But you can also use your own background image too. just replace "red.jpg" with yours. "Saturate(200%)" gives a saturation effect to the pictures used(red.jpg).  Line 363 "animation: Gradient 20s ease infinite;" is the part where "red.jpg" is animated. "Ease infinite" lets  a continuous loop to the animation. If you delete this part the animation of the red background will stop and there will only be a static red background behind the picture.

 Line 412 is the place of spotify post place

![image](https://user-images.githubusercontent.com/84282504/226617473-22b8aa4a-2cdc-4647-958e-20e788274f75.png)

This is not a text but an image. 

Double clicking this spotify text will also hide boolean " input_boolean.modern_dashboard_spotify_card_hide_media_players" which is related with the above media players. 

![image](https://user-images.githubusercontent.com/84282504/226617956-91769ea3-3d9d-4ebf-ab35-caa87ab20bb7.png)

Line 446 is the the place where play sign appears. 

![image](https://user-images.githubusercontent.com/84282504/226618130-257230e1-bc80-4422-afbb-39abcea92a83.png)

## Room Presence Music:

This feature is activated with an automation. It is a simple and easy one. What it does is when it is activated through a button the automation checks the sensor and finds out the last room you entered. After that, with a help of an automation it starts to play Spotify music on that rooms media player.

To achieve that we need 3 things: 

- Spotcast integration to be installed.
- A input Button named "input_button.modern_dashboard_spotify_last_room_music"
- [Last Room Motion template sensor](https://github.com/berkansezer77/home-assistant/blob/main/pages/spotify-card-v2/last-room-motion)
- [Last Room Music Automation](https://github.com/berkansezer77/home-assistant/blob/main/pages/spotify-card-v2/last-room-music-automation)

1) Ceate your button from helpers section of Home Assistant.
2) Enter template sensor code into configuration.yaml or sensor.yaml(if you have a seperate sensor.yaml section). 

Reload Template entities in developers tools section of HA. 

![image](https://user-images.githubusercontent.com/84282504/226622661-a7617a63-8783-4dbf-a487-f5144e1ba3a8.png)

3) Create the given automation above. Don't forget to change motion sensor names with your own ones. This autoamtion is based on my setup. 

Now everything is ready. When we press the play icon on the Play icon the music will automatically start on the last room we entered. Don't forget that we can also start music individually from the topbar media player icons. Just tap any media player icon you want the music to start and it will execute straight away. Double tapping the icon will also stop the media player. 


## Media Player:

When music starts a media player will appear in the page. That media player starts from the line 477. It will only appear when Spotify is on "Paused" or "Playing" status. This is because the media player has an album art cover. This album art cover only appears when Spotify is in "Paused" or "Playing" status. When it goes to "Idle" the album art disappears. So in my setup when it passed to idle the welcome screen will appear. 

The media player has controls of play, pause,stop, next and volume. It is a mushroom based media player card. 

Line 569 has the progress bar card. Due to mushroom media player has not progress bar but mini player does it is being used in here. 

![image](https://user-images.githubusercontent.com/84282504/226630142-2724233b-bcb3-4290-9547-0f72fb0fcea2.png) 

You can change the color of the bar in line 595. Just change "amber" to any color you like. 

## Card Mode animation (line 641): 

The media player card has a same understanding with the welcome page. It is applied to the whole card with the help of card mode. Card mode copies album art work. It creates a second one behind the album art cover. When you change line 654 "blur(100px)" to "blur(1px)" you can easily see the album art cover behind the media player. 

![gif5](https://user-images.githubusercontent.com/84282504/226632702-31eb669c-5581-4e08-9725-f4bf0841c1b1.gif)

But when you change it back to 100px it blurs the whole image and only colors will be visible. 

![gif6](https://user-images.githubusercontent.com/84282504/226633596-7a576964-db00-49a4-8be2-95ba07e40c81.gif)

Since it uses the album cover, the colors on the page match perfectly with the music.

"animation: Gradient 12s linear infinite;" is where the animation starts. change 12s to your like to slow or fast movements of the background picture. 

"background-size: 70% 70%;" is the size of the background picture. If you change it to a number like "100% %100" the picture will grow and this will let the lights to cover all page. Try it yourself.

Line 670 is the rotation path. 

If you enjoy my work check out my other pojects and please star this page on github. 

Enjoy....



