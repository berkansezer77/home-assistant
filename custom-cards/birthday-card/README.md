_**If you like you can support my work.**_

<a href="https://www.buymeacoffee.com/berkansezer" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a> 

# Birthday Card
<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/8f80dd53-c6e7-4815-a72a-473f53650de5" width="350">
<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/c774ebb4-0398-4f87-9d04-1a0b48febfea" width="300">
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

Ok let's start. First of all we need to have a google calendar integrtion ready for the birthdays to appear in Home Assistant. You can find various videos on Youtube for the installation. 

If you have installed google calendar a birthday calendar calendar should be visible in your entegrations page. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/779ff3a4-0661-484d-807b-c5f57e0ec4e4)

When you enter the integration you will see that a birthday calendar is there. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/47d5503c-c21a-4762-9b50-272114e2a5dc)

In my case it is called calendar.dogumgunleri. Okay it is in Turkish but generally it is the calendar for the birthdays. When you click the calendar : 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/9fef4ada-b164-4146-a450-00a4725c50ad)

You will see that it will only give you on - off state. If you check for the details from HA menu developers tools > state you will see that it will give you a single birthday information which is the current or upcoming birthday from your calendar. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/5e6976d1-e20e-4807-a98b-0739606fc7b4)

Now we need to create a new sensor which will display next 4 birthdays from this Google Calendar. But before doing I am going to show you how you can create a new birthday info for any person .

1) click on this address
![image](https://github.com/berkansezer77/home-assistant/assets/84282504/81c8acc1-f445-4323-8c27-11a7909c499b)
2) Click upper left "Create a new Person" icon.
![image](https://github.com/berkansezer77/home-assistant/assets/84282504/635cf2c3-a587-4c7f-894b-36c2765cfd9d)
3) Enter the necessary information and don't forget to complete birthday section.
4) Now go back to HA integrations page and refresh Google Calendar
![image](https://github.com/berkansezer77/home-assistant/assets/84282504/c7c5b63a-5d93-4d91-a428-1d451c435568)







