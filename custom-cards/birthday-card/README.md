_**If you like you can support my work.**_

<a href="https://www.buymeacoffee.com/berkansezer" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a> 

# Birthday Card
<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/8f80dd53-c6e7-4815-a72a-473f53650de5" width="350">
<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/c774ebb4-0398-4f87-9d04-1a0b48febfea" width="250">
<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/a7502f86-67ea-4680-92bc-f8e68018c261" width="350">


# Installation

**How much time does it take to install this. ? **

It takes about 20 - 30 minutes. It depends on how many people's birthday you want to display on your dashboard. But remember, you only do it once. 🎉

**How do I install this theme?**

This not a python or anything else coded software but just a code. 

**This is hard because I don't have any code knowledge.**

Don't worry. I have a manual for setup. Everything is explained there and it is super easy to install. 

**Where are the codes ? **

Everything you need including the setup manual is in this page. 🎉

**I don't have the multimedia files you used. ? **

For this project you do not need any multimedia files. Because it is a birthday card you have to create your own. Instructions are in the manual. 🎉
## Page Properties:

- Displays 4 upcoming birthdays. The number can also be increased further with the help of a swiper card
- Shows the remaining time for birthdays. 
- Ready for White and Dark Theme.
- Highlights the birthday person in a white frame. 
- Birthday icon at the very first card let's HA to remind you the birthday in various ways. In my example a notification through telegram.
- Full screen tablet version

## Before we start, we need some third party tools from Hacs:

- [Layout Card](https://github.com/thomasloven/lovelace-layout-card)
- [Card Mod](https://github.com/thomasloven/lovelace-card-mod)
- [Stack in Card](https://github.com/custom-cards/stack-in-card)
- [Mushroom Card](https://github.com/piitaya/lovelace-mushroom)

You will also need the Google Calendar integration to be installed in Home Assistant.
[Link: ](https://www.home-assistant.io/integrations/google/)


##Templates and Automations: 

Wen need some templates and 1 single automation for the code to function properly. You use yaml to create templates but if you want to use my method which explained in the manual you must have at least Home Assistant version 2023.09.

Templates: 
- [Remaining Days](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/birthday-card/remaining-date-template)
- [Birthday Message](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/birthday-card/birthday-message-template)
- [Yaml Calendar Sensor](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/birthday-card/yaml-birthday-template)

Automations:
- [Reminder Automation](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/birthday-card/reminder-automation)

## Page Code: 

#Mobile
  
To install the page you need this code: [Page Code](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/birthday-card/page-code-mobile)

#Tablet

To install the page you need this code: [Page Code](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/birthday-card/page-code-tablet)

## Manual : 

COMİNG SOON
