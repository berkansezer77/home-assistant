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

You will see that it will only give you on - off state. If you check for the details from HA menu developers tools > state you will see that state attributes will give you only a single birthday information which is the current or upcoming birthday from your calendar. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/9b4e8297-9993-46fc-8ddb-f7264915bf9d)

Now we need to create a new sensor which will display next 4 birthdays from this Google Calendar. But before doing I am going to show you how you can create a new birthday info for any person .

1) click on this address
2) 
![image](https://github.com/berkansezer77/home-assistant/assets/84282504/81c8acc1-f445-4323-8c27-11a7909c499b)

4) Click upper left "Create a new Person" icon.

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/635cf2c3-a587-4c7f-894b-36c2765cfd9d)

4) Enter the necessary information and don't forget to complete birthday section.
5) Now go back to HA integrations page and refresh Google Calendar

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/c7c5b63a-5d93-4d91-a428-1d451c435568)

6) When you check your HA calendar(on left menu). The newly created person birthday will be shown there.

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/10a3f496-7a27-42f1-8854-c1be45e93d6d)

Okay now let's get back to our code. Now as I said we need to create a new template for next 4 upcoming birthdays. So put down below code to your configuration.yaml

- [Yaml Calendar Sensor](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/birthday-card/yaml-birthday-template)

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/cd6612ad-1a3f-4fdd-bf5a-966a3ce26479)

Restart Home Assistant. After reboot you will see that a new sensor is being created. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/b0801196-f0e5-407e-8319-b57d79a8491f)


Now as you see from the developers menu a bunch of people's next birthday information is listed in state attributes. So we need to extract only 4. If you plan to show more then 4 then there is a way too but I will show you that later. 

Now we need to extract the name of the birthday person first. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/fe041562-61de-4e82-b198-2ad872369621)

As you can see the name is "Emre Bora Kiztan adlı kişinin doğum günü". So this means "Birthday of Emre Bora Kiztan " Sorry I couldn't find a way to convert it to English and that is because HA is displaying the data from Google in my local language. But I will show you the way to shorten this sentence. 

We need a template for this. The template is quite simple. 

```ruby
{{ state_attr('sensor.calendar_scheduled_events', 'scheduled_events')[0].summary | replace("adlı kişinin doğum günü", "") }}
```
So I will explain this code. It is very simple. "sensor.calendar_scheduled_events" is the new sensor we just created which displays multiple people's birthday. 

The name we should derive is on state's attribute which is "Summary" so next line in the code "[0].summary" takes the very first person's birthday. 

Remember the newly created sensor displays birthdays to date order. So "0" means the first birthday. 

"| replace("adlı kişinin doğum günü", "")" this code replaces sentence "adlı kişinin doğumgünü" with and empty(""). So as a result, normally the very first birthday atrrbute message was "Emre Bora Kiztan adlı kişinin doğum günü" but "| replace("adlı kişinin doğum günü", "")" this little part cuts off "adlı kişinin doğum günü" sentence so the new outcome appears as only the name is displayed which is "Emre Bora Kiztan". So if in English it is the as "Birthday of Merve Koç" try the replace line like this, "| replace("Birthday of", "")" this will cut the "Birthday of" sentence and only the name will be displayed.

So now we need to create a sensor for that. With Home Assistant 2023.09 wen can now create sensors inside helpers section shortly from the UI. 

So go to helpers menu.

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/8585b644-93fa-441d-bdfd-a63ad19e3a0a)

Click plus icon(Create Helper) on the bottom right and choose "Template" and then "Template a sensor" 

Put the above code into "state template*" area and save it. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/95868daa-aae1-44c2-8265-fa203cd9149c)


the outcome should be like this. If everything is ok our sensor will give you below infotmation. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/83eb918e-0182-4117-b4f7-ddf246905385)


As you can see only the name is being displayed. 

So now we have created our first birthday card sensor. But we need to display 4 person. So 3 more left. Do the same process above and create 3 more templates. But be careful. you need to change 0 in the code :

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/ece1f676-253c-4701-8f9a-3690154f5e52)

0 here displays the first birthday data from the sensor. But in our second card we should change zero with 1. 

```ruby
{{ state_attr('sensor.calendar_scheduled_events', 'scheduled_events')[1].summary | replace("adlı kişinin doğum günü", "") }}
```
1 is the second upcoming birthday from the list which is Volkan Aksoy. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/bf6bd738-f326-4c6f-9308-217a4ce669b9)

So second template sould look like this. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/bc7b6627-361e-4ccf-9454-1117d5fec041)

Ok now do it for 3rd and the last sensor. Don't forget the change the number to 2 for the third and 3 for the last one. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/6f03f43f-bd94-4f13-a66b-fca9eff21655) 

Now we have 4 sensors ready 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/a731c666-8d1a-4b72-8af6-333189156103)

So now let's move on to date sensors. Again we create 4 sensors from the helpers section. 

```ruby
{{ state_attr('sensor.calendar_scheduled_events', 'scheduled_events')[0].start }}
```

This will take the starting date from the very first birthday person. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/58f41553-6223-44e0-a545-fc7879f9526f)

When you create sensors ıt will display the time. Again as a reminder. "0" is the first birthday person in our sensor. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/75114e16-2a6d-48bb-9961-e4ba779f5ca2)














