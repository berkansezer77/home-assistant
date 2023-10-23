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

For this project you do not need any multimedia files. Since this is a birthday card, you must upload person photos yourself. 🎉
## Page Properties:

- Displays 4 upcoming birthdays. The number can also be increased further with the help of a swiper card
- Shows the remaining time for birthdays. 
- Ready for White and Dark Theme.
- Highlights the birthday person in a white frame. 
- Birthday icon at the very first card, let's HA to remind you the birthday in various ways. In my example a notification through telegram.
- Full screen tablet version
- Info on creating a sensor that displays multiple birthdays
- Info on creating the template sensors from the UI
- Info on how to shorten state attribute messages.
- Info on creating full screen content on tablet and pc view.
- Full code explanation line by line

## Before we start, we need some third party tools from Hacs:

- [Layout Card](https://github.com/thomasloven/lovelace-layout-card)
- [Card Mod](https://github.com/thomasloven/lovelace-card-mod)
- [Stack in Card](https://github.com/custom-cards/stack-in-card)
- [Mushroom Card](https://github.com/piitaya/lovelace-mushroom)

You will also need the Google Calendar integration to be installed in Home Assistant.
[Link: ](https://www.home-assistant.io/integrations/google/)


##Templates and Automations: 

Wen need some templates and 1 single automation for the code to function properly. You can also use yaml editing for templates, but you must have at least Home Assistant 2023.9 ​​version for the methods I explain in the user manual.

Templates: 
- [Remaining Days](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/birthday-card/remaining-date-template)
- [Birthday Message](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/birthday-card/birthday-message-template)
- [Yaml Calendar Sensor](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/birthday-card/yaml-birthday-template)

Automations:
- [Reminder Automation](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/birthday-card/reminder-automation)

## Page Code: 

#Mobile
  
To install the mobile version you need this code: [Page Code](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/birthday-card/page-code-mobile)

#Tablet

To install the tablet version you need this code: [Page Code](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/birthday-card/page-code-tablet)

## Manual : 

Ok let's start. First of all we need to have a "Google Calendar" integration ready for the birthdays to appear in Home Assistant. You can find various videos on Youtube for the installation. 

If you have installed google calendar a birthday calendar should be visible in your integrations page. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/779ff3a4-0661-484d-807b-c5f57e0ec4e4)

When you enter the integration you will see that a birthday calendar is there. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/47d5503c-c21a-4762-9b50-272114e2a5dc)

In my case it is called "calendar.dogumgunleri". The name is Turkish, but its function is to pull the birthday information from your Google contacts and show it to you.

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/9fef4ada-b164-4146-a450-00a4725c50ad)

You will see that it will only give you the on - off state. If you check for the details from HA menu developers tools > state, its current structure displays only one single upcoming birthday information.

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/9b4e8297-9993-46fc-8ddb-f7264915bf9d)

So we need to create a new sensor which will display next 4 birthdays from this Google Calendar. But before doing I am going to show you how you can create a new birthday info for any person .

1) click on this address

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/81c8acc1-f445-4323-8c27-11a7909c499b)

2) Click upper left "Create a new Person" icon.

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/635cf2c3-a587-4c7f-894b-36c2765cfd9d)

3) Enter the necessary information and don't forget to complete birthday section.
4) Now go back to HA integrations page and refresh Google Calendar

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/c7c5b63a-5d93-4d91-a428-1d451c435568)

6) When you check your HA calendar(on left menu). The newly created person birthday will be shown there.

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/10a3f496-7a27-42f1-8854-c1be45e93d6d)

# Yaml Template Calendar Sensor

Okay now let's get back to our code. Now as I said we need to create a new template for next 4 upcoming birthdays. So put down below code to your configuration.yaml

- [Yaml Calendar Sensor](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/birthday-card/yaml-birthday-template)

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/cd6612ad-1a3f-4fdd-bf5a-966a3ce26479)

Restart Home Assistant. After reboot you will see that a new sensor is being created. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/b0801196-f0e5-407e-8319-b57d79a8491f)


Now as you see from the developers menu a bunch of people's next birthday information is listed in state attributes. So we need to extract only 4. 

# Name Sensors

Now we need to extract the name of the birthday person first. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/fe041562-61de-4e82-b198-2ad872369621)

As you can see the name is "Emre Bora Kiztan adlı kişinin doğum günü". So this means "Birthday of Emre Bora Kiztan " Sorry I couldn't find a way to convert it to English and that is because HA is displaying the data from Google in my local language. But I will show you the way to shorten this sentence. 

We need a template for this. The template is quite simple. 

```ruby
{{ state_attr('sensor.calendar_scheduled_events', 'scheduled_events')[0].summary | replace("adlı kişinin doğum günü", "") }}
```
This code is pretty simple. "sensor.calendar_scheduled_events" is the name of the new sensor we just created which displays multiple people's birthday. 

What we shall seek inside this sensor is the  "Summary" part. So next line in the code "[0].summary" takes the very first person's birthday. 

Remember that the newly created sensor displays birthdays up to date order. So "0" stands for the first birthday. 

"| replace("adlı kişinin doğum günü", "")" 

The above part erases the words "adlı kişinin doğumgünü" with an empty statement using (""). 

So as a result, while getting and atrribute message "Emre Bora Kiztan adlı kişinin doğum günü" we cut the sentence with :

<i><font color="red">| replace("adlı kişinin doğum günü", "")</i></font> part. 

This little trick leaves the attribute message as "Emre Bora Kiztan" which is the name of the person. 

So if in English it is the as "Birthday of Merve Koç" try the replace line like this, 

<i>| replace("Birthday of", "")</i>

this will cut the "Birthday of" from the sentence and only the name will be displayed.

So now we need to create a sensor for that. With Home Assistant 2023.09 wen can now create sensors from helpers section shortly from the UI. 

So go to helpers menu.

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/8585b644-93fa-441d-bdfd-a63ad19e3a0a)

Click plus icon(Create Helper) on the bottom right and choose "Template" and then "Template a sensor" 

Put the above code into "state template*" area and save it. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/95868daa-aae1-44c2-8265-fa203cd9149c)


The outcome should be like this. If everything is ok our new sensor will contain the below information. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/83eb918e-0182-4117-b4f7-ddf246905385)


As you can see only the name is being displayed. 

So now we have created our first birthday card sensor. But we have 4 person cards. So 3 more left. Do the same process above and create 3 more templates. But be careful. you need to change 0 in the code :

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/ece1f676-253c-4701-8f9a-3690154f5e52)

0 here displays the first birthday data from the sensor. But in our second card we should change zero with 1. 

```ruby
{{ state_attr('sensor.calendar_scheduled_events', 'scheduled_events')[1].summary | replace("adlı kişinin doğum günü", "") }}
```
1 is the second upcoming birthday from the list which is Volkan Aksoy. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/bf6bd738-f326-4c6f-9308-217a4ce669b9)

The second template will look like this.....

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/bc7b6627-361e-4ccf-9454-1117d5fec041)

Ok now do it for 3rd and the last sensor. Don't forget the change the number to 2 for the third and 3 for the last one. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/6f03f43f-bd94-4f13-a66b-fca9eff21655) 

Now we have 4 sensors ready 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/a731c666-8d1a-4b72-8af6-333189156103)

# Date Sensors

So now let's move on to date sensors. Again we create 4 sensors from the helpers section. 

```ruby
{{ state_attr('sensor.calendar_scheduled_events', 'scheduled_events')[0].start }}
```

This will take the starting date from the very first birthday person. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/58f41553-6223-44e0-a545-fc7879f9526f)

When you create sensors it will display the time. Again as a reminder. "0" is the first birthday person in our sensor. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/75114e16-2a6d-48bb-9961-e4ba779f5ca2)

Do the same process for other three sensors. 

2.
```ruby
{{ state_attr('sensor.calendar_scheduled_events', 'scheduled_events')[1].start }}
```
3.
 ```ruby
{{ state_attr('sensor.calendar_scheduled_events', 'scheduled_events')[2].start }}
```
4.
```ruby
{{ state_attr('sensor.calendar_scheduled_events', 'scheduled_events')[3].start }}
```
So the creation of 4 date sensors is as follows : 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/7d41dfa5-7175-48e6-8ef1-5aac91fd2977) 

# Remaining Time Sensors

Now and last we need to create date remaing sensors. We do it from the same spot "helpers section".

```ruby
{% set midnight = now().replace(hour=0, minute=0, second=0, microsecond=0).timestamp() %}
{% set event = as_timestamp(states('sensor.calendar_birthday_schedules_date_1')) %}
{% set delta = ((event - midnight) // 86400) | int %}
{% if delta == 0 %}
  Today
{% elif delta == 1 %}
  Tomorrow
{% elif delta == 2 %}
  2 days
{% elif delta == 3 %}
  3 days
{% elif delta == 4 %}
  4 days 
{% elif delta == 5 %}
  5 days 
{% elif delta == 6 %}
  6 days
{% elif delta == 7 %}
  7 days
{% elif delta == 8 %}
  8 days
{% elif delta == 9 %}
  9 days
{% elif delta == 10 %}
  10 days 
{% else %}
 Far Away
{% endif %}
```
This part will give us the remaing days in numbers for the person who has a birthday. 

Again place the above sensor into the template sensors as we have done before. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/77edb1d3-550c-42d0-bcb0-ff5ba926b242)

This time this template takes the date from previously created "date sensors" and displays the remaing days. Again we need 4 of them and we have only created first one. So we have to repeat the same process 3 times. 

Rmeaing sensors are : 

2.
```ruby
{% set midnight = now().replace(hour=0, minute=0, second=0, microsecond=0).timestamp() %}
{% set event = as_timestamp(states('sensor.calendar_birthday_schedules_date_2')) %}
{% set delta = ((event - midnight) // 86400) | int %}
{% if delta == 0 %}
  Today
{% elif delta == 1 %}
  Tomorrow
{% elif delta == 2 %}
  2 days
{% elif delta == 3 %}
  3 days
{% elif delta == 4 %}
  4 days 
{% elif delta == 5 %}
  5 days 
{% elif delta == 6 %}
  6 days
{% elif delta == 7 %}
  7 days
{% elif delta == 8 %}
  8 days
{% elif delta == 9 %}
  9 days
{% elif delta == 10 %}
  10 days 
{% else %}
 Far Away
{% endif %}
```
3.
```ruby
{% set midnight = now().replace(hour=0, minute=0, second=0, microsecond=0).timestamp() %}
{% set event = as_timestamp(states('sensor.calendar_birthday_schedules_date_2')) %}
{% set delta = ((event - midnight) // 86400) | int %}
{% if delta == 0 %}
  Today
{% elif delta == 1 %}
  Tomorrow
{% elif delta == 2 %}
  2 days
{% elif delta == 3 %}
  3 days
{% elif delta == 4 %}
  4 days 
{% elif delta == 5 %}
  5 days 
{% elif delta == 6 %}
  6 days
{% elif delta == 7 %}
  7 days
{% elif delta == 8 %}
  8 days
{% elif delta == 9 %}
  9 days
{% elif delta == 10 %}
  10 days 
{% else %}
 Far Away
{% endif %}
```
4.
```ruby
{% set midnight = now().replace(hour=0, minute=0, second=0, microsecond=0).timestamp() %}
{% set event = as_timestamp(states('sensor.calendar_birthday_schedules_date_3')) %}
{% set delta = ((event - midnight) // 86400) | int %}
{% if delta == 0 %}
  Today
{% elif delta == 1 %}
  Tomorrow
{% elif delta == 2 %}
  2 days
{% elif delta == 3 %}
  3 days
{% elif delta == 4 %}
  4 days 
{% elif delta == 5 %}
  5 days 
{% elif delta == 6 %}
  6 days
{% elif delta == 7 %}
  7 days
{% elif delta == 8 %}
  8 days
{% elif delta == 9 %}
  9 days
{% elif delta == 10 %}
  10 days 
{% else %}
 Far Away
{% endif %}
```

So everything is set. We have succesfully created the remaing day sensors. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/b3ddc0a0-daff-43e8-97f6-10d8c493ca6d)

# Code explanation 

So lets explain our code line by line
Line 11 - 34 is where the little crown icon stands. With this you can turn on and off notifications for the birthdays. Below you can find the automation code. 

- [Reminder Automation](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/birthday-card/reminder-automation)

In this automation I used  a telegram notification for reminders. Birthdays are saved as "All day events" so this automation sends a notification 30 minutes before midnight(previous day at 23:30) reminding me that a birthday will be active in 30 minutes. You can use anything you like for the reminder. For example you can let specific lights turn on or get an email. I also used a boolean to be turned on for this automation to work. The boolean is named "input_boolean.live_tiles_birthday_automation". You have to create it from helpers section choosing "Toggle". So when we press the "crown" icon at top left this automation becomes active. 

Line 35 - 94 is for 2 little information on the birthday card. The name of the birthday person and the days left to his birthday in numbers. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/2f529cc6-459c-4db0-8e09-e6eaa658f019) 

You can tweak this area by playing ".primary" and ".secondary" settings which is located at line 51 and line 65. For example you can the color background of "Days remaing" at line 73. You can also play with font size at Line 53 and Line 66. Also font family can be changed at Line 58 nad Line 71.

Line 95 - 144 is the part where our first cards inside picture and other properties are written. Now this part is important. For example at Line 114 card takes the birthday person name and checks with the data starting from Line 115. If there is a match it displays the photo on entire card. 

Let's look at our example 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/cae2cc7d-4c29-48f7-ad8c-551bed399156)

Line 114 checks the state from "sensor.calendar_birthday_schedules_msg_1" and the result of that sensor is :

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/5e93d2fd-80eb-4778-83f2-9235b310b7e9)

Line 117 contains information of a person named Emre Bora Kiztan. So because the sensor "sensor.calendar_birthday_schedules_msg_1" result is "Emre Bora Kiztan", the photo at Line 118 will be used in the card until "sensor.calendar_birthday_schedules_msg_1" displays another name. In other words until the birthday is over. 

Line 119 will also check "time remaining" to the birthday. If the state is "Today" it will highlght entire card. This way you will know that there is a birthday on the current day.

So 

```ruby
{% elif state=='Emre Bora Kiztan' %}
  background:  url( '/local/png/birthday/emrebora.png' ) no-repeat center 0px;
```
This code is for one person only. Below is the position of that person's photo inside the home assistant. To add a new one you have to create another "elif state" like the this. 

```ruby
{% elif state=='Emre Bora Kiztan' %}
  background:  url( '/local/png/birthday/emrebora.png' ) no-repeat center 0px;
{% elif state=='Berkan Sezer' %}
  background:  url( '/local/png/birthday/berkan.png' ) no-repeat center 0px;
```

Be careful: 

- The name written here should exactly be the same with "sensor.calendar_birthday_schedules_msg_1" result. Case sensitivity is also important. For example "Emre Bora Kiztan" should not be "Emre Bora kiztan" otherwise the photo will not be displayed.

  ![image](https://github.com/berkansezer77/home-assistant/assets/84282504/06522202-53ef-4b8b-919a-d5c9cea722d7)

- Local characters are also important. like lets say if you use "ı" instead of "i" the photo again won't be displayed.

Tips: 

-Try to copy the name from "sensor.calendar_birthday_schedules_msg_1" and paste it into the name area at the code. With this way you won't make any mistake. 
- To get a persons photo use their social media. Find a proper picture and take a screenshot and save into your HA birthday folder(Or if you gave a different folder name for the photos, put them in that folder.)

Line 145 - 262 is the second card. The process is exactly the same with the first one. You need to add all the names you entered on the first card to the second card. So for a simple way when you finish adding names to the first card copy them and paste into the second card. 

Line 263 - 380 is the third card.

Line 381 - 499 is the last and final card.

## Tablet view 

I have also added a tablet view with full screen photos. 

[Tablet view](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/birthday-card/page-code-tablet)

To display the card properly we need "Layout Card" and some adjustments. 

1) Create a separate tab in your dashboard.

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/788c9f9f-8154-4e4a-b79e-fa025774b218)

Enter below code into "Subview section"

```ruby
grid-template-columns: auto 0px 0%
grid-template-rows: auto
grid-template-areas: |
  "header header header"
  "main . sidebar"
  "footer footer footer"
mediaquery:
  "(max-width: 600px)":
    grid-template-columns: 100%
    grid-template-areas: |
      "header"
      "sidebar"
      "main"
      "footer"
  "(max-width: 800px)":
    grid-template-columns: 50% 50%
    grid-template-areas: |
      "header sidebar"
      "main main"
      "footer footer"

```
After that just copy and paste the code into the page. The structure is exactly the same with mobile only some modifications has been made in order to display the photos with full size. 

