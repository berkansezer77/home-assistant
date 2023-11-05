_**If you like you can support my work.**_

<a href="https://www.buymeacoffee.com/berkansezer" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a> 

# Animated Home Assistant Weather Card
<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/b25fa791-609a-4584-b55d-e727a0c40456" width="350">
<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/3970648e-bc7e-4140-b169-a9a93d2b25a8" width="250">
<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/ff020cea-6be0-4af6-a95c-81b54297b04b" width="200">
<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/5ecc44d4-ef6c-4a8d-a8d9-35746f5c3a15" width="150">


Before we begin I was very much inspired by the work of "Weather App" design by "Hua". I thought this will be the best design to give life. I coded bunch of details and I hope you will enjoy it.

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

- Fully animated
- Can be used with any weather station unless the provide specific weather info. (see manual page for what this card requires)
- White and Dark Theme Ready
- 5 day Forecast
- Hourly Forecast
- Detailed Weather info
- Short Weather Report
- Ability to turn off animations
- Fully customizable through using the manual provided.
- All the multimedia files are included
- Manual includes information about pulling information from weather attributes. Use any data you like
- Fully dynamic
- Single click change from dark to white or vice versa

## Before we start, we need some third party tools from Hacs:

- [Layout Card](https://github.com/thomasloven/lovelace-layout-card)
- [Mushroom Card](https://github.com/piitaya/lovelace-mushroom)
- [Card Mod](https://github.com/thomasloven/lovelace-card-mod)
- [Stack in Card](https://github.com/custom-cards/stack-in-card)
- [Browser Mode](https://github.com/thomasloven/hass-browser_mod)

You will also need a weather service. In my template I am using weather Met.no and Openweather service.
[Openweather](https://www.home-assistant.io/integrations/openweathermap/)
[Met.No](https://www.home-assistant.io/integrations/met/)

## Booleans:

I used 8 booleans, 1 template and 1 automation. Create booleans from helpers section. Don't forget to select "Toggle" in the helpers section. 

- input_boolean.theme
- input_boolean.weather_report
- input_boolean.weather_animations
- input_boolean.weather_card_details
- input_boolean.weather_card_weekly
- input_boolean.weather_card_weekly
- input_boolean.weather_card_hourly
- input_boolean.weather_card_details

And the sensor is located at : It will be explained in the manual. 

[12 hour rain probability](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/weather-card/12-hours-rain-probability)

## Video:

[Home Assistant Custom Weather Page](https://www.youtube.com/shorts/UCNNxIdTHHg)

## Page Code: 

- To install the page you need this code: [Page Code](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/weather-card/page-code)

## Multimedia Files
[Download the necessary files from this link](https://www.dropbox.com/scl/fi/gmbp29o5nvjytxnqfw2ly/Weather.zip?rlkey=5brdaa0d4fo95ft06hdwb3mda&dl=0)

## Manual:

It is very easy to install this template. First of all we need to learn how to change from dark and white theme. 

##Change Theme:

To change the theme with a signle click, Browser Mode should be installed and we need to create an input boolean named "input_boolean.theme". Changing the theme from white to dark is quite easy. Just follow the steps. 

1) Download "Google White Theme" from Hacs.
2) Download Mushroom Shadow from Hacs.
3) Register your browser. To do that go to browser mode in side menu and click register this browser.
4) Now we need 2 scripts and 1 automation. After that a single click will change the mode.

[Script White Mode](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/spotify-card-v2/page-code)

[Script Dark Mode](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/spotify-card-v2/theme-google-light-script)

[Automation](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/spotify-card-v2/dark-and-white-mode-automation)

![1](https://github.com/berkansezer77/home-assistant/assets/84282504/3f0c795c-f181-467a-9bdc-972f8a1ea812)


Now the boolean we created before(input_boolean.theme) is ready for transformation between themes. The onlu thing you need is you should place tap action into anywhere you like to single click and change the whole theme. 

As shown in above example, changing theme is available with a double click to "Suadiye" word at the upper left corner. The code for that click is: 

```ruby
                tap_action:
                  action: call-service
                  service: input_boolean.toggle
                  target:
                    entity_id: input_boolean.theme
```
In out page code this line is at Line 20

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/a9d8abf7-5a75-456f-a723-5f95b361cc53)

## Code Explanation:

Line 5 - 133 : 

This is the upper part where it is giving location info with date and chips for opening report page and animations at the right. starting from line 92 has the "report icon" which opens reports for today's and tomorrow's weather inside the middle screen. This is tied to a boolean called "report" at line 103 and this boolean opens with a single tap action at line 104.
![image](https://github.com/berkansezer77/home-assistant/assets/84282504/431e1474-9be9-4257-8f4a-6dfa82fbde8b)

So when you press this icon the screen in the middle will display weather report like this 

![2](https://github.com/berkansezer77/home-assistant/assets/84282504/fc5c174a-3abd-462d-96f8-530796a7388d)

Same process will happen with the "Drop" icon. This time middle screen will start to show animations. A boolean "input_boolean.weather_animations" is used here. 

![3](https://github.com/berkansezer77/home-assistant/assets/84282504/0a80ddd1-b990-4425-971e-9d232f9f3589)

Line 134 - 360: 

This is the place where middle screen is located. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/5eb30a1f-2119-4130-a6d4-9ac0ce5887dd)

line 136 to 199 includes the degree information which is taken straight from my outdoor temperature sensor. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/62208719-cc7f-4b55-a408-822948bc709e)

If you don't have an outdoor sensor you can use your any weather station sensor. To do that just replace line 150. "|int" is used to round the result coming from the sensor. For example if it is 29.97 the result will be shown as 29. The styling of the degree is located between line 162 and 174. For example you can change the font size at line 167. The second "Sunny" part is the "secondary" part between lines 176-185. If you want to change ffont you can add "font-family: "Formula1-regular";" into primary or secondary parts. 

Line 200 - 273 is where weather report will be shown. As you remember we were activating these cards from the top menu. I used a markdown card for this area. All the details shown in this card can be customized. For the general weather at line 212 I am taking "the real feel" temperature info from openweather app. So you may use your own or if you want to use mine, "Openweather" map should be installed. 

# Retrieve info from attributes:
Now I will show you have to derive information from a weather attribute. For example Met.no weather integration shows as entites like this : 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/519e1eca-4348-4a70-af9d-1be505ab0f0b)

So there are lots of info here. The lines starting from "forecast:" are the days info. Today's date is 28.10 so : 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/6c61ec5e-65cb-42d2-8144-095cc8ef9a1f)

As you can see on line 15 "datetime" it is shown as 28. So it means today. The next one is tomorrow which is 29. And this continues with the other dates. So take the info from today's wind speed we should use a code like this : 

```ruby
{{ state_attr('weather.forecast_home', 'forecast')[0].wind_speed }}
```

This will give "20.2" as a result. So "o" is the first day here and the ".wind_speed" is the windspeed data from the first day which is today. So if you want to take let's say tomorrow's wind speed data you should change "0" with "1" like this : 
```ruby
{{ state_attr('weather.forecast_home', 'forecast')[1].wind_speed }}
```

This will give tomorrow's estimated wind speed result. 

So back to our code. As you can see I have taken datas from the list with the above method. Now you know how to do it you can customize it with other weather services. You can use any other with the template. 

At Line 239 I use my own template to retrieve next 12 hour rain probability. So you have to create this at helpers section. Choose create helper>template>template a sensor. The sensor code is here [12 hour ain template](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/weather-card/12-hours-rain-probability). copy this code and paste it into state template section. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/d86671c9-09fe-4880-9029-e45ddaaffc28)

Click submit and now you will have a new sensor with the name "sensor.weather_next_12_hours_rain_probability" 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/8bb08e4b-0f8f-4808-8ed9-816f38fcc9f3)

Don't forget this function is only available after Home Assistant 2023.09 so if you are using lower versions of Home Assistant you should create this sensor from the yaml.

Line 274 to 360 is where the card mode happends. The animations used in the card is here. If you want to use your own animations change the gif's in this area. For example if you want to use a different "Sunny Weather" gif just go to line 326 and write down your multimedia files local adrress. 

Line 361 - 491 : 

This is where the animation in the middle screen appears. It is dynamic and changes up to the weather conditions. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/3ce1b075-7f45-4213-89b7-3e69fd6b8198)

If you want to change the size play with host section starting at line 485.

Line 492 - 906: 

This is where additional weather information can be found. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/445d95db-a825-460e-94e8-1a074cc628e3)

This section is hidden and can be activate by pressing to "Details" button 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/c1d069ee-5da5-42e5-9407-b22f0dd9cbd1)

I already showed you how to take information from attributes so you can customize this section with any inf you like. 

For example 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/25d60841-4ffe-446f-9e25-447d97129b03)

At line 769 we take wind speed from the above list with the code 

```ruby
  {{  state_attr('weather.forecast_home','forecast')[0].wind_speed  }}
```

This is today's wind speed. But you may want to replace this with tomorrow's wind_bearing data. So the new code will be : 

```ruby
  {{  state_attr('weather.forecast_home','forecast')[1].wind_bearing }}
```
So "1" used in the code is for tomorrow and wind bearing is the data for tomorrow's "wind_bearing"

Line 907 - 1107 

is the place where Weekly - Hourly  and Detais tabs exist. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/7b3fb78c-c347-4958-b062-4584cf8ec96f)

This section will show you the appropriate information for the selected tab. For example if you have selected "Weekly" then upcoming days weather information will be shown. 

Ok these tabs open weekly and hourly data. But when you open them both, both weekly and hourly data will be shown under each other. Normally when weekly tab opens weekly data the hourly tab should close. In order to achieve that we need an automation. 

[Weekly-Hourly Tab Automation](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/weather-card/weekly-hourly-tab-automation)

Because I used a conditional card for weekly and hourly data, create this automation so that when one tab opens other ones can close. 


![image](https://github.com/berkansezer77/home-assistant/assets/84282504/c5dd2338-ef69-4f8c-bfaf-9d8c6a572e0e)

Line 1108 - 1574 

This section shows you weekly information in a button shaped interface. There is a 5 day's forcast info including the day we are in. This can be extended into more days maybe with a help of "Swipe Card". 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/98a8f294-c057-42a8-9e38-e99cf50e8da7)

It is very simple. "Primary" is the date conversion from weather attributes. 

```ruby
{{ as_datetime(state_attr('weather.forecast_home','forecast')[0].datetime,).strftime('%a')  }}
```

0 Here stands for today. "Secondary" info takes temperature from today's atrributes and the "picture" is the little animated icon at the top. If it is sunny the "SUNNY" icon will shown there. Icons and all other multimedia staff are can be downloaded from the link below. You can also use your own gifs or icons as well. But trust me these are beatiful.

[Download the necessary files from this link](https://www.dropbox.com/scl/fi/9d76daycfro8i3ex85389/Weather.zip?rlkey=ofz0qb4pgkcg530lfwf9d1zoe&dl=0)

Line 1575 - 2026 

Are last section. Like the previous one this one now shows hourly weather info. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/441a9dbd-3e4a-4989-84cf-8455c8544f68)

As you can see it show the weather for the coming hours in a three hour interval. 

```ruby
  {{as_datetime(state_attr('weather.forecast_home_hourly','forecast')[5].datetime,).strftime('%H:%M')}}
```

Starts with the 5.th section of "weather.forecast_home_hourly" then goes with 3 hours interval. So to show 3 hours ahead we need to use number "8" with the next hour. This way if it is 5pm the for the card "5" to show 8pm we need to move up to "8" because hourly attributes are showing every hour. So next card to show 8pm is : 

```ruby
  {{as_datetime(state_attr('weather.forecast_home_hourly','forecast')[8].datetime,).strftime('%H:%M')}}
```
You can change the look of the time. "('%H:%M')" As you can see with this H and M the time displays as "20:00" but it can also be displayed as "20PM". There is a good information the community written by pedro. 

[Custom Timestamps](https://community.home-assistant.io/t/convert-date-and-time-template/99328)

So this is it. I hope you enjoyed it. If yes please give me a star on github. Thank you very much for reading and showing attention to my projects. 





