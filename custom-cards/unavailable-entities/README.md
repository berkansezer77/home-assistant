_**If you like you can support my work.**_

<a href="https://www.buymeacoffee.com/berkansezer" target="_blank"><img src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png" alt="Buy Me A Coffee" style="height: 41px !important;width: 174px !important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5) !important;" ></a> 

## Unavaliable Entites:
![1](https://github.com/berkansezer77/home-assistant/assets/84282504/4539a74d-a228-4213-850f-3d1423fef3e8)

<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/1b7a01aa-eed3-4d45-a54c-e044ca5cf5d2" width="450">

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

2 - You have to create an ignore Group. If you have a seperate "group.yaml" file copy and paste the code down below to your group.yaml file. 

[Ignored Entites Code ](https://github.com/berkansezer77/home-assistant/blob/main/custom-cards/unavailable-entities/unavailable-entities-sensor.yaml)

It should look like this...

<img src="https://github.com/berkansezer77/home-assistant/assets/84282504/7f2f2cf9-142c-45ad-bb82-7bee04c10375" width="250">


İmportant Note: When you first create the code you will see that a lot of unavailable devices will be displayed. That sometimes doesn't mean that the integration or device is not working. For example Smartthings integration brings your Samsung TV to home assistance. You control your TV, turn it on and off but some extra enttites such as energy monitoring are unavaliable. 

![image](https://github.com/berkansezer77/home-assistant/assets/84282504/5b8a2cc7-a90f-43af-a932-17b4b2ccee57)

In that case just add entity names to the ignored groups you have a created. You can also disable these entites from HA. If you disable an offline entity it will also not appear in your unavailable list as well. 

Some buttons may also seem to be offline although they are completely fine and working. You can also add them to the list.

3) Restart home assistant

4) Copy my code to your dahsboard. And your new chip will be ready. 
