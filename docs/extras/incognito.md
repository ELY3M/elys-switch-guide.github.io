## Incognito


## Enabling Incognito in atmosphere 0.12.0 or above 
Atmosphere devs added in this nice thing.
more info/changelog at [https://github.com/Atmosphere-NX/Atmosphere/releases/tag/0.12.0](https://github.com/Atmosphere-NX/Atmosphere/releases/tag/0.12.0)

!!!warning "Caution"
	This will 100% stop online play or any game or firmware updates from happening if it is enabled. 
	This is designed for totally offline emunands.   
	
1. download `exosphere.ini` from [here](https://raw.githubusercontent.com/Atmosphere-NX/Atmosphere/master/config_templates/exosphere.ini)
2. open exosphere.ini in notepad or your favorite text editor.  

look at the section in bottom of exosphere.ini

<pre>
[exosphere]
debugmode=1
debugmode_user=0
disable_user_exception_handlers=0
enable_user_pmu_access=0
blank_prodinfo_sysmmc=0
blank_prodinfo_emummc=0
allow_writing_to_cal_sysmmc=0
</pre>


3. if you are only running CFW in emunand.  you can change this line blank_prodinfo_emummc=0 to blank_prodinfo_emummc=1  
   if you want to make sysnand offline for some reasons, use this line blank_prodinfo_sysmmc=0 and change it to blank_prodinfo_sysmmc=1 (not recommeneded)
4. save exosphere.ini and put it on the root of your sd card.   
5. reboot atmosphere via reboot by payload or rcm method.   




<!--
!!! danger "Warning:" 	
	- Incoginito_RCM is dangerous and will wipe serial and parts of your prodinfo in your switch nand.  It will make your switch totally offline and wont be able to access Nintendo services at all.      
	- it is same as Super Ban.  it will not be able to do normal firmware updates.   
	- Make sure you do your NAND backup before doing incognito.   
	- Do NAND back up, if you have not done your nand backup.  The nand backup guide is [here](/../extras/nandbackup)
	- I know several people who made their switches "Super Banned" due to running incognito without doing prodinfo and nand backups.  
	- one person sent his console to Nintendo and get patched unit.   
	- very important to select emummc to incognito if you want to make your emummc totally offline and keep sysnand clean and online.   
	
## What is Incognito_RCM	

This is from their github.  
Incognito_RCM is a bare metal Nintendo Switch payload that derives encryption keys for de- and encrypting PRODINFO partition (sysnand and emummc) and wiping personal information from your Nintendo Switch as to go online while worrying slightly less about a ban.
It has a builtin backup and restore functionality.

It is heavily based on [Lockpick_RCM](https://github.com/shchmue/Lockpick_RCM) and takes inspiration from [incognito](https://github.com/blawar/incognito).

Massive Thanks to CTCaer, shchmue and blawar!

This project is in early stage, so have a nand backup!!

Usage
=
* Launch Incoginito_RCM.bin using your favorite payload injector
* Use menu to make a backup! (Will be written to `sd:/prodinfo_sysnand.bin` and `sd:/prodinfo_emunand.bin` respectively)
* Choose Incognito (emuMMC) to wipe personal information from your emunand/emuMMCs
* If you ever want to revert, choose restore menu points
	
Screenshots
=

Main            |  Incognito
:-------------------------:|:-------------------------:
![](/extras/incognito/main.png)  |  ![](/extras/incognito/incognito.png)

Backup            |  Restore
:-------------------------:|:-------------------------:
![](/extras/incognito/backup.png)  |  ![](/extras/incognito/restore.png)





### What you need:
- The <a href="https://github.com/jimzrt/Incognito_RCM/releases" target="_blank">Incognito_RCM</a> Payload

### Instructions:

!!! tip ""
    1. Copy `Incognito_RCM.bin` to the `/bootloader/payloads` folder on your SD card	
    2. Enter RCM and inject the Hekate payload
	3. Tap the `Payloads` option, then press Incognito_RCM.bin.
	4. Backup both sysnand and emummc prodinfos by selecting Backup in the menu
	5. reboot back to RCM and put your sd card in your computer.   
	6. copy the `sd:/prodinfo_sysnand.bin` and `sd:/prodinfo_emunand.bin` files and save them in safe place.  best to keep them with where you keep your nand backups.   
	7. put sd card back in your switch.  
    8. inject the Hekate payload
	9. Choose Incognito (emuMMC) to wipe personal information from your emunand/emuMMCs
	10. reboot back to RCM AND Inject the fuse-primary.bin to boot atmosphere.  
	11. go to system settings and check the serial info. it should be blank like in the image below here.     



![](/extras/incognito/after.png)

-->













