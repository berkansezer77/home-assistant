_**If you like you can support my work.**_

<a href="https://www.buymeacoffee.com/berkansezer" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a> 

Unavaliable Entites

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/956529d8-7c15-48ee-ba73-b6a24686a265)
![image](https://github.com/berkansezer77/home-assistant/assets/84282504/2b16d120-e9f7-4412-b231-a922ac60fd52)

## Page Properties:

- Displays the list of offline entites in the topbar
- Dynamic icon that changes with the number of unavailable entities. If nothing is offline the icon changes.
- Browser Mod support. If you click the icon a new page, containing the list of unsupported devices will appear. 
- Number Display. You will see the number of the offline devices inside the chip.

## What we need ?:

- Mushroom Cards: [Mushroom Cards](https://github.com/piitaya/lovelace-mushroom)
- Browser Mode : [Browser Mode](https://github.com/thomasloven/hass-browser_mod)
- Hui- Element : [Hui Element](https://github.com/thomasloven/lovelace-hui-element)
- Card Mod: [Card-Mode](https://github.com/thomasloven/lovelace-card-mod)

## Download Multimedia files:

The Wifi icon is located at : 

- Files are located at: [Multimedia files](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/unavailable-entities/offline.png)

Page Code: 

- To install the page you need this code: [Page Code](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/unavailable-entities/page-code)

_## Manual_

1 - First we have to create a little template in sensor.yaml(If you didn't seperate it then paste into config.yaml). Just copy and paste the code.

[Sensor Code ](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/unavailable-entities/unavailable-entities-sensor.yaml)

2 - You have to create an ignore Group. If you have a seperate group.yaml file copy and paste the code down below to your group.yaml file. 

ignored_entities:
  entities:
      - button.ewelink_ds01_identify  (Example)
      - button.banyo_kap_sensoru_identify_3 (Example)
 
If you don't have just copy and paste the code to your configuration.yaml

group:
  ignored_entities:
    entities:
      - button.ewelink_ds01_identify (Example)
      - button.banyo_kap_sensoru_identify_3 (Example)

İmportant Note: When you first create the code you will see that a lot of unavailable devices will be displayed. That sometimes doesn't mean that the integration or device is not working. For example Smartthings integration brings your Samsung TV to home assistance. You control your TV, turn it on and off but some extra enttites such as energy monitoring are unavaliable. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/5b8a2cc7-a90f-43af-a932-17b4b2ccee57)

In that case just add the entity names to the ignored groups you have a created. Also some buttons may seem as offline althought they are completely fine and working. You can also add them to the list.

3) Restart home assistant

4) Copy my code to your dahsboard. And your new chip will be ready. 
