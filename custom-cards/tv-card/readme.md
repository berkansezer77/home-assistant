_**If you like you can support my work.**_

<a href="https://www.buymeacoffee.com/berkansezer" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a> 

# Home Assistant TV Card 
<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/6c47923e-129d-4c6d-a942-4ad2e69b410c" width="250">
<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/68c2d146-cb62-451a-873e-27166ed75dce" width="200">
<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/2b7715c7-f8d6-418a-9523-841843bc85ca" width="200">
<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/2a6e3b9d-daeb-417a-a32f-7d5988ffc1ce" width="150">

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

I don't actually know from where to start. This card has tons of features. 

- Ability to control both TV and the Android TV at the same time
- Live view. See what is playing on your Android TV screen with pictures. (Streaming services like Netflix don't allow passthrough images due to copyrights)
- Remote controls for Samsung TV and Android TV
- Ability to start Hue light integration with a single click. Even the official hue integration of HA does not have this future. 
- Start Apps directly from the card (Works both on Samsung and Android TV apps)
- See which apps are currently on
- Media Controls for Samsung TV, Change HDMI, Switch sound between soundbar and TV, Turn on Ambient Mode and change Picture Mode
- Show you cameras on Android TV with a click to a button
- Switch between Android Tv and Samsung TV remotes with a single click
- Information area about what is happening on your Android TV or Samsung TV
- Turn on your Samsung or Android TV with a single click
- Browse and start your favorite Netflix show straight from the card
- All Multimedia files are included.
- Start listening your favorite radio stations on your Android TV
- Whatever device is active on the television screen, the remote control of that device is shown on the card. If the input on the TV screen changes, your card will also automatically switch to that card.
- You can also launch some apps from your Android TV remote.
- Remotes are fully customizable you can assign your own remote controls via scripts.
- The card will show you which device is being shown on your TV screen at that exact momemnt.
- Full installation manual available
- Dark and White theme compatible
- You can use your Own IR device and bring any button to your remote control. You are not only tied to the Samsung integration.


## Before we start, we need some third party tools from Hacs:

- [Layout Card](https://github.com/thomasloven/lovelace-layout-card)
- [Mushroom Card](https://github.com/piitaya/lovelace-mushroom)
- [Card Mod](https://github.com/thomasloven/lovelace-card-mod)
- [Stack in Card](https://github.com/custom-cards/stack-in-card)
- [Mini Media Player](https://github.com/kalkih/mini-media-player)
- [Swipe Card](https://github.com/bramkragten/swipe-card)
- [Firemote Card](https://github.com/PRProd/HA-Firemote)
- [Vertical Stack Card](https://github.com/ofekashery/vertical-stack-in-card)

Integrations: 

You will also need some integrations in order this card to work properly.

From Hacs: 
[Samsung TV Smart](https://github.com/ollo69/ha-samsungtv-smart)

From Home Assistant:
[Smartthings](https://www.home-assistant.io/integrations/smartthings/)
[Generic Camera](https://www.home-assistant.io/integrations/generic/)
[Android TV integration](https://www.home-assistant.io/integrations/androidtv/)

## Booleans, Scripts and Automations:

This card needs some automations and scripts to function properly and booleans are also important. 
So for the full list of booleans used in the code are down below. 

- input_boolean.tv_page_shield
- input_boolean.theme
- input_boolean.tv_page_shield_radio
- input_boolean.tv_page_shield_netflix
- input_boolean.tv_page_shield_remote
- input_boolean.tv_page_shield_apps
- input_boolean.tv_page_samsung
- input_boolean.tv_page_samsung_media
- input_boolean.tv_page_samsung_remote
- input_boolean.tv_page_samsung_apps

  These booleans are for the passage between the menus. When a menu is on the other should be closed and this is done with an help of an automation.

  So we need 3 automations for this card:

- [Auto Change Remote on Dashboard](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/tv-card/auto-change-remote-on-dashboard)
- [Auto Close Tabs Samsung](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/tv-card/auto-close-tabs-samsung)
- [Auto Close Tabs Shield](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/tv-card/auto-close-tabs-shield)

## Page Code: 

The full code this TV-Card is : 

[Page Code](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/tv-card/page-code)

## Multimedia Files: 

Multimedia Files are also located at : 

[Download Files](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/tv-card/tv-card.zip)

## Manual:

Please read the manual before you install this card. Remember, this card provides much more than just a control mechanism. It encompasses numerous automations, scripts, and features. Every detail is provided to you in this user guide.

The card itself contains 2 separate remotes. One for Samsung TV and the other one is for Shield TV. The transition between 2 remotes can be made from one single card. This card also has white and black theme support. Additionally you switch between white and dark theme with a single click (or double click in our example). 

So Let's start with theme change. 

##Change Theme:

To change the theme with a signle click, Browser Mode should be installed and we need to create an input boolean named "input_boolean.theme". Changing the theme from white to dark is quite easy. Just follow the steps. 

1) Download "Google White Theme" from Hacs.
2) Download Mushroom Shadow from Hacs.
3) Register your browser. To do that go to browser mode in side menu and click register this browser.
4) Now we need 2 scripts and 1 automation. After that a single click will change the mode.

[Script White Mode](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/tv-card/change-to-white-mode-script)

[Script Dark Mode](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/tv-card/change-to-dark-mode-script)

[Automation](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/tv-card/dark-and-white-mode-automation)

<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/668c6cb5-cee5-4af9-ba7f-c69e3a45cb1f" width="250">

Now the boolean we created before(input_boolean.theme) is ready for transformation between themes. The only thing you need is you should place tap action into anywhere you like to single click(or double click) and change the whole theme. 

As shown in above example, changing theme is available with a double click to "Samsung" or "Shiwld TV" word at the upper left corner. The code for that click is: 

```ruby
                tap_action:
                  action: call-service
                  service: input_boolean.toggle
                  target:
                    entity_id: input_boolean.theme
```
In out page code this line is at Line 37

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/23ac04f1-c330-45b6-9ac8-8eb6926dba83)

## Code Explanation:

Before delving into the code, I mentioned to you that this card consists of two separate sections. Now, in terms of the code, the first section, from line 1 to line 2278, is dedicated to the Shield TV remote. The section from line 2278 to line 4112 contains the necessary codes for controlling the Samsung TV. 
If you delete the portion from line 2278 to line 4107, you will be left with only the Shield TV remote section. I will share the necessary code for a single remote control with you at the end of this article.

So to seperate 2 sections we need 2 conditional cards boosted with booleans. So in order to do that create 2 booleans named "input_boolean.tv_page_shield" and "input_boolean.tv_page_samsung" from the helpers section. Remember to choose "Toggle" 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/9705df0b-0344-4b83-ba2c-347ebc99bd75)

So we start with shield TV. Line 5 indicates that only the section related with "Shield TV" will be shown. 

If you want to pass to Samsung remote just press "Shield" at the menu and "input_boolean.tv_page_samsung" will be turned on "input_boolean.tv_page_shield" will be turned off. So you will only see the items related to your TV. 

![source changegif](https://github.com/berkansezer77/home-assistant/assets/84282504/b8d8bcff-dd0b-49c5-81a6-0c3a1f977e0d)

Of course, we need an automation to prevent both cards from appearing on the screen at the same time

- [Auto Close Tabs Shield](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/tv-card/auto-close-tabs-shield)

Okay let me explain this automation. It might seem a bit complex but at its base it is very simple. I have added 6 automations in to 1 single automation using "Choose". So they are triggers here. 
For example 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/85267691-4bb1-4440-b721-8015213038f6)

first one is when tv page shield netflix changes to on. I have given this trigger an id named "Netflix"

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/c2002759-86c1-497e-96b9-4eb1612dbc18)

So if come down at "Action" section. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/7b4fc9d0-2e84-4fa3-b8aa-2e4dd4842056)

The first action on "Choose" will be a result of what will happen when you click Netflix section. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/2fc9aa83-d7dc-4440-9d4d-5fd35f36779c)

When you click it below actions will execute. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/a980461e-d042-41c6-a8dc-4cf67c45433e)

As you can see Shield remote, Shield apps and Shield radio sections will be closed and you can only see "Netflix" part on your Shield Remote Page. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/e1382b26-a9a3-4e26-9ace-52608c7c9bff)

Choose 2,3 and 4  are all related to that menu. Very Simple. When you click for example "Remote" section the other 3 booleans will close and only remote will be shown on screen. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/2e705ca1-26c3-4d54-9414-9bc2b22d6884)

We will come to that part.

Choose 5 and 6 actions are the transiton part between "Samsung TV" and "Shield TV" cards. So when you press Samsung the whole card will be transformed into Samsung remote. 


So Let's get back to the code. 

so Line 20 will show a card when your SHield TV is on 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/b357251c-bc3e-4499-b6dc-7b24c113ac98)

Line 37 as I explained before will have a double tap function which changes your theme color from black to white or vice versa. If you like you can assign this function to a single tap action with deleting from line 32 to 36 amd change Line 37 from "double_tap_action:" to "tap_action:". So a single press to "Shield TV" section will change the theme. 

Line 45 have the card mode functions. Line 48 is where "Shield TV" sign stands. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/7edcfa56-1b7e-4d40-9e82-e7d7b08a8f0b)

You can modify this section from Line 48 to Line 62. For example you can change the font type by editing "font-family: 'Georgia';" on Line 58. You can extend the red box editing its "width: 140px !important;" You can also change the background of the box with "background: rgba(252, 3, 32, 2.6) !important;". To find the right rgba code just search google with "color picker". Then choose your correct color and take rgb values 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/f6596694-951d-41cf-aa33-9248768d5aaa)

Then paste it into "background: rgba(252, 3, 32, 2.6) !important;" code. For example if you choose the purple color for this box background color the correct code will be as 
"background: rgba(168, 50, 166, 2.6) !important;"

Line 81 is the place when your "Shield TV is off" 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/b2fbcb61-d869-486e-b73e-8f041fbb39f7)

I Used a mushroom chips card here to start Shield TV

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/2f0936b3-bf55-4eac-be28-8e0c6fc736f2)

You can again tweak this box settings starting from line 100. For example you make the background color as red with changing "--chip-background: rgba(var(--rgb-blue)," to "--chip-background: rgba(var(--rgb-red),"

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/7a9c10a5-4e0a-4480-a70a-20b570e3c616)

At line 94 there is a little script assigned to this box. It lets the shield TV to turn on. I am using Android Debug Bridge to control Shield TV on Home Assistant. So to turn on Shield just use a little script. The script below also turns on my amplifier. 
Here is the script 

```ruby
alias: Samsung TV - On
sequence:
  - service: scene.turn_on
    data: {}
    target:
      entity_id: scene.anfi_ac
  - delay:
      hours: 0
      minutes: 0
      seconds: 1
      milliseconds: 0
  - type: turn_on
    device_id: a94021e0fe601d5599dd53fad87c10bf
    entity_id: 7baee18b5d7fc5ebbd8147c8fa3f2c84
    domain: switch
mode: single
icon: mdi:television

```

Just create a simple script for turning on the TV and call it from line 98.

Okay Line 127 shows your android TV screen. I used a custom mini-media player to reflect android screen to this card. "artwork: full-cover" shows what is going on the screen. There is a little lag for the image to refresh at this card. They are some other ways to fasten this process but for me a 20s lag is ok. So the image fits the screen when android TV is on. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/60ab26af-8f36-4c71-9ef7-962416d5590a)

There is one important thing here. You cannot get live screen views from streaming services like Netflix. This is due to copyright issues. Netflix even does not allow to show its menu. This means when you click and start Netflix app on Android TV a blank screen will appear as cover. It will also stay black until you exit Netflix. Disney and Prime Video lets you get screenshots while you are in their menu but they do also block image whenever a video is played. So in order to bypass the screen to be empty at line 176 I used a little if statement to fill the screen with picture while Netflix is "ON". You can find this if state at Line 177 "background: url('/local/png/tv-card/cover.png') center no-repeat;" and can change the screenshot with your own by changing "cover.png" On line 182 you see "box-shadow: 0px 0px 10px 5px rgba(255,255,255, 0.96) !important;" little box shadow which covers the screen area. You can change the color here from white to any color you like. Just play around with numbers. 

Line 188 is the place where little icon box stands.

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/2e21017d-e571-4f45-9ccb-eaa3774170c5)

This box contains the icons of the apps and changes according to the app that is active on screen. It is controlled by an if state starting from line 248. So if you want to change or add something just edit lines between 248 and 286.

Line 306 is the template for the info screen. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/c039c8b9-fee6-4fc6-b26a-5bc02eccc76d)

This little info part gives you exact info of the app and hdmi port. For example if your TV is on it's smart menu, lets say Samsung TV is currently showing Tizen Smart Apps, then this little info screen will warn you about what the screen is currently showing. But if you change to hdmi to android tv, this info screen will warn you that you are currently on hdmi showing Android Menu. Also other apps like Netflix or Disney will also be shown on this info screen. Unfortunately because Samsung TV integration does not display playing or pause status but only on or off, streaming information won't be available for Samsung TV. You will only see "Currentlu on TV Screen" information whenever you are on Samsung Menu. 

This information part exist in the codes between the lines 309 and 376

Line 393 to 450 will have the changes for this info screen. You can play a little bit and change style. For example changing "font-family: "Arial";" to something else will change fontstyle. Again you can play a little bit with the values here to your liking.  

Line 451 is the place where 5 main headers start. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/97ab7d15-1428-4dd5-a65f-37bce0a32991)

Line 460 is the Radio part. 

On line 471 tapping into Radio word will activate radios section of Android TV. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/60adadf5-a008-4b7c-bd80-bcff1bfb008f)

When tapped other parts such as Netflix, Remote and Apps will be closed. This is done by an automation I explained before. 

To understand which tab you are currently in the section will be highligted and others will be grayed out. Line 484 to 491 will determine the conditions of this section under white and dark modes. On white mode the color will be blue which is at line 486. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/f9f12d9b-0c04-432a-8848-4059a1962d7a)

On line 461 is the place where little dot appears. 
![image](https://github.com/berkansezer77/home-assistant/assets/84282504/2ffc54ed-b040-4036-bfbf-87f1239ded67)

The styling and position of this dot is at line 504. For example if you want the dot to be a little bigger you have to tweak Line 509 and line 511. Remember this dot will only be shown for the active tab at that moment. For others the visibility will be hiddden. This is stated at line 507 "visibility: hidden;"

Line 531 is the "Netflix" tab. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/2c8a9c72-2ce5-4a61-89e2-18e7a033b734)

Line 554 is the place where you can tweak "Netflix" word and line 575 is again the little dot. 

Line 596 will show "Remote" tab.

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/4af7ee3f-e533-422e-b485-72be3a3c89bd)

Line 662 will show you "Apps" tab.

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/e3fee516-5209-4028-ae37-aa6aacb4430c)

Once again in order for these tabs to work properly you need to have the automation as I previously mentioned before. Try to create the booleans with the same names I have given to them. 

Line 733 is the tab where you can change the whole card view from Shield TV to Android TV. 

As I mentioned before ".primary" and ".secondary" parts in each tab code will let you play with the tab appearance(color,style,font etx..)

So when you press "Samsung" here you are now viewing the Samsung Remote card. 

<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/09bb7ed0-b174-485d-8df6-6d33069085b0" width="200">

From line 804 now we start to create content under these tab menus. First we start with "Netflix" Section. I used a swipe card here at line 818 and all the posters extends into second and third page. You can swipe between pages.

So Our first show is "Raising Dion" which starts at line 839. This show is activated with a script. Script is simple : 

```ruby
alias: Start Blacklist
sequence:
  - service: androidtv.adb_command
    data:
      command: >-
        am start -n com.netflix.ninja/.MainActivity -a
        android.intent.action.VIEW -e amzn_deeplink_data 80143529
    target:
      entity_id: media_player.shield
mode: single
icon: mdi:television

```
Okay now everything is very simple. Open Netflix on your pc browser. Find your favorite show. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/5ddffa13-0cf5-4962-be5f-03b098138a15)

As you can see in the picture "80143529" is the code for TV Show "Blacklist". So your script is ready. Let's get back to the code 

Line 839 is where you put blacklist or any other show. with a tap action on line 842 you are calling the script you created for your favorite show. Whenever you press the poster the show will automatically start on your Android TV. One good benefit of this script is it bypasses the netflix account page and starting the show immediately from where you have left. And for the final part you need the poster for the show. That is the easiest thing. Just find a poster from the internet and replace line 841 with that. Remember you need to copy the image link from the picture. You don't even have to store the image locally.  

So I used a grid layout with 3 posters next to each other (Line 836). Next page starts at line 977. And the last page is at Line 1121. 

Line 1243 is the closure of this section. If you don't like the blue color between the posters just replace line 1246 with for example "background: none;" so no color will be shown here. 

Line 1249 is where the remote for Shield TV stands. I used a firemote card which is quite useful. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/20303d1a-79b9-45d8-a611-0487be5e21f1)

Firemote card has basic controls for Shield Tv, Apple Tv and many others. It is fully customizable. As you can see in the code I have also customized the remote controls. Line 1275 is the place where my button overrides starts. that means my buttons are customized and don't have the original codes with firemote card. I used my own scripts to over ride these cards. For example I used my own script for "Mute Button". The benefit here is, if you have an ir controller such as Tuya or Broadlink you can use those ir buttons on this remote. 

```ruby
alias: Samsung TV - On
sequence:
  - service: scene.turn_on
    data: {}
    target:
      entity_id: scene.anfi_ac
  - delay:
      hours: 0
      minutes: 0
      seconds: 1
      milliseconds: 0
  - type: turn_on
    device_id: a94021e0fe601d5599dd53fad87c10bf
    entity_id: 7baee18b5d7fc5ebbd8147c8fa3f2c84
    domain: switch
mode: single
icon: mdi:television

```










