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

## Page Code: 

Multimedia Files are also located at : 

[Download Files](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/tv-card/tv-card.zip)


