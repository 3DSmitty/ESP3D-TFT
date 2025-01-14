<span align="left"><img src="https://github.com/luc-github/ESP3D-TFT/blob/main/logo/ESP3D.png" width="200px"/></span><span align="left">ESP3D-TFT Firmware for ESP32 based TFT  </span>    
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[<img src="https://img.shields.io/liberapay/patrons/ESP3D.svg?logo=liberapay">](https://liberapay.com/ESP3D)

## Features
A Serial TFT with all WiFi feature to control 3D Printer or CNC, using same feature as [ESP3D](https://github.com/luc-github/ESP3D/tree/3.0)     

Unlike ESP3D some features will be fixed:
* Flash FS = littleFS
* TBD

## UI

To be defined, it will use lvgl library in espressif IDF 4.X (TBD)  

## Reference boards

The reference boards I have bought :

* ESP32 based + SDReader + 2.8'resistive screen (240x320) [model](https://www.aliexpress.com/item/3256804315935867.html) (Received)
* ESP32-S3 based + SDReader + PSRAM + 4.3' capacitive screen  (800x600) [model](https://www.aliexpress.com/item/1005003814428825.html) (Received)
* ESP32-S3 based + SDReader + PSRAM + 3.5' capacitive screen (320x480) [model](https://www.aliexpress.com/item/1005004309826174.html) (Received)
* ESP32 + SDReader + 3.5' Resistive screen (480x320) [Rotrics TFT](https://rotrics.com/products/3-5-inch-touchscreen) (Received)
* TBD...

## installation
- Install the IDF vs code extension
	- https://github.com/espressif/vscode-esp-idf-extension/blob/master/docs/tutorial/install.md
- Configure the extension
	- Select : View->Command palette 
	- Type : configure esp
- Open TFT-ESP3D project
	- Go to file and select open folder where project is located
- Edit CMakeLists.txt to select the correct target, be sure your Device target and port are properly set in espressif extension. (esp32 / esp32s3)

## Project's sources structure
```
- ESP3D-TFT/   
             - CMakeLists.txt   
             - components/ - lvgl/ -...   
			   - littlefs/ -...  
			   - network/ -...  
			   - gcodeHost/ -...  
	     - main/ - core/ - esp3d-tft.cpp   
			     - includes/ - esp3d-tft.h   
					 - CMakeLists.txt
					 - components.mk
					 - main.cpp
					 - version.h
             - targets/ - ESP32_2432S028R/ - components/ - sdkconfig
				                         - partitions.csv
							 - lvgl/ - CMakeLists.txt
							         - components.mk
							         - lv_conf.h
							 - lcd/ - CMakeLists.txt
							        - components.mk
							        - ...
							 - touch/ - CMakeLists.txt
							          - components.mk
								  - ...
			- ESP32_ROTRICS_DEXARM35/ -...
			- ESP32S3_HMI43V3/ -...
			- ESP32S3_ZXD50CE02S_USRC_4832/ -...
```
## Todo

Everything, code from scratch or almost
* Design UI (Flow + icon)
* Code UI / navigation 
* Add WiFi features
* Add Streaming Features
* TBD... 

## Chat

Please use discord : [![discord](https://img.shields.io/discord/752822148795596940?color=blue&label=discord&logo=discord)](https://discord.gg/Z4ujTwE)

## :question:Any question ?   
Check [Wiki](https://github.com/luc-github/ESP3D/wiki/Install-Instructions) or Join the chat at [![Discord server](https://img.shields.io/discord/752822148795596940?color=blue&label=discord&logo=discord)](https://discord.gg/Z4ujTwE)   

## :exclamation:Any issue/feedback ?    
Check [Wiki](https://github.com/luc-github/ESP3D-TFT/wiki) and [FAQ](https://github.com/luc-github/ESP3D-TFT/discussions/categories/q-a) 
If you still have issue: [submit ticket](https://github.com/luc-github/ESP3D-TFT/issues)    
If it is not an issue join some discussion [here](https://github.com/luc-github/ESP3D-TFT/discussions)

## Sponsors 
[<img width="200px" src="https://raw.githubusercontent.com/luc-github/ESP3D-WEBUI/2.1/images/sponsors-supporters/MKS/mksmakerbase.jpg" title="MKS Makerbase">](https://github.com/makerbase-mks)&nbsp;&nbsp;

## Supporters

## Become a sponsor or a supporter
 * A sponsor is a recurent donator    
   As my sponsorship is not displayed by github your logo / avatar will be added to the readme page with eventually with a link to your site.    
 * A supporter is per time donator 
   To thank you for your support, your logo / avatar will be added to the readme page with eventually with a link to your site.  

 Every support is welcome, indeed helping users / developing new features need time and devices, donations contribute a lot to make things happen, thank you.

* liberapay <a href="https://liberapay.com/ESP3D/donate"><img alt="Donate using Liberapay" src="https://liberapay.com/assets/widgets/donate.svg"></a> 
* Paypal [<img src="https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG_global.gif" border="0" alt="PayPal – The safer, easier way to pay online.">](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=FQL59C749A78L)
* ko-fi [![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/G2G0C0QT7)   
