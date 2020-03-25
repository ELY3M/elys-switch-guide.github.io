# Switch Guide for Atmosphere

A guide collaboration between Nintendo Homebrew's Helpers and Staff, from stock to Atmosphere.

### Credits and Thanks
I took [this guide](https://switchgui.de) and modified it to make it more simpler, less steps, and have more extra guides for common things done on Switch CFW.  

Thank you very much to those people below here.  

ELY M.    

&nbsp;

The original guide at [https://switchgui.de](https://switchgui.de)
This guide was written by staff members of the [Nintendo Homebrew Discord Server](https://discord.gg/C29hYvh) 

&nbsp;

!!! tip "Credits"
    **SciresM, TuxSH, hexkyz, fincs, Flump, jerbear64, Phoenix, xGhostBoyx, Such Meme Many Skill, and oreo639.**

    Thank you to [everyone else](https://github.com/nh-server/switch-guide/graphs/contributors) that contributed to the guide on GitHub, but special thanks to **noirscape**.

!!! tip ""
    [You can find this guide on GitHub](https://github.com/nh-server/switch-guide), It is licensed under the [ISC license.](https://github.com/nh-server/switch-guide/blob/master/LICENSE.md)


!!! tip "Developer / Tool credits"
	- **ReSwitched** for some of texts in the guides [ReSwitched discord]()
    - **Atmosphere-NX** for [Atmosphere](https://github.com/Atmosphere-NX/Atmosphere).
    - **switchbrew** for [nx-hbloader](https://github.com/switchbrew/nx-hbloader) and [nx-hbmenu](https://github.com/switchbrew/nx-hbmenu).
    - **nwert** and **CTCaer** for [Hekate](https://github.com/CTCaer/hekate).
    - **WerWolv** for [EdiZon](https://github.com/WerWolv/EdiZon/releases).
    - **Flagbrew** for [Checkpoint](https://github.com/FlagBrew/Checkpoint).
    - **mtheall** for [FTPD](https://github.com/mtheall/ftpd/).
    - **joel16** for [NX-Shell](https://github.com/joel16/NX-Shell).
    - **Cease & DeSwitch** for [fusee-gelee](https://github.com/Qyriad/fusee-launcher).
    - **MenosGrante** for [Rekado](https://github.com/MenosGrante/Rekado).
    - **eliboa** for [TegraRcmGUI](https://github.com/eliboa/TegraRcmGUI).
    - **vgmoose**, **pwsincd**, **rw-r-r_0644** and **crc32** for [hb-appstore](https://github.com/vgmoose/hb-appstore).
    - **exelix** for [NXThemes Installer and SwitchThemeInjector](https://github.com/exelix11/SwitchThemeInjector).
    - **Essometer** for collecting patched Switch serials.
    - **shchmue** for [Lockpick](https://github.com/shchmue/Lockpick/releases) and [Lockpick_RCM](https://github.com/shchmue/Lockpick_RCM/releases).
    - **Ave** for [90DNS](https://gitlab.com/a/90dns).
    - **Nexrem (meganukebmp)** for the [Switch 90DNS Tester](https://github.com/meganukebmp/Switch_90DNS_tester).
    - **exelix11** for [Switch Theme Injector](https://github.com/exelix11/SwitchThemeInjector/releases).
    - **vgmoose** for [hb-appstore](https://github.com/vgmoose/hb-appstore).
    - **ITotalJustice** for [atmosphere-updater](https://github.com/ITotalJustice/atmosphere-updater).
	- **noahc3, Team AtlasNX** for some of texts and ideas from [The Ultimate Noob Guide for Hacking your Nintendo Switch](https://switch.homebrew.guide/index) 
	- **XorTroll** for [Goldleaf](https://github.com/XorTroll/Goldleaf)  
	- **huntereb** for [Awoo-Installer](https://github.com/Huntereb/Awoo-Installer)
	- **developersu** for [ns-usbloader](https://github.com/developersu/ns-usbloader)
	- **Joonie86** for [Sigpatches](https://github.com/Joonie86/hekate/releases/tag/5.0.0J)
	- **spacemeowx2** for [Lan-play](https://www.lan-play.com)



&nbsp;


### What is homebrew?

!!! tip ""
    Homebrew applications are custom, user-made software, which haven’t been authorised by Nintendo. This can include save editing tools, games, emulators, and more.

    Homebrew can be run for free on your Switch as long as you have a "first-generation" system running 9.2.0 or lower, and a USB-C cable.

### What is Custom Firmware?

!!! tip ""
    Custom Firmware (“CFW”) enables you to use more advanced hacks that userland homebrew can’t easily do. For instance, installing game modifications with ease.

    CFW can be set up on any first-generation console on any version (but will require additional tools).

### What does this guide install?

!!! tip ""
    This guide has the end goal of taking a completely unmodified Switch from Stock Firmware to Atmosphere Custom Firmware.

    fusee-gelee is currently the best method of launching Custom Firmware that gives us nearly full control of the system. It utilizes a vulnerability in the bootROM of the first-generation Switch systems, allowing us to send any payload we want to the Switch's recovery mode, instead of only ones that Nintendo have authorized.

### What can I do with Custom Firmware?

!!! tip ""
    * Customize your HOME Menu with user-created themes and splash screens
    * Use “ROM hacks” for games that you own
    * Backup, edit, and restore saves for many games
    * Use cheats for your games and make the cheats for your games.  
	* Use games mods and make game mods, for Ex: Super Mario Odyssey mods at [https://gamebanana.com/games/6376](https://gamebanana.com/games/6376)
    * Play games for older systems with various emulators, using RetroArch or other standalone emulators
    * Safely update to the latest system version without fear of losing access to homebrew

### What do I need to know before starting?

!!! tip ""
    Before beginning the guide, you must know the risks of Switch hacking: EVERY time you modify your system, there is always the potential for an UNRECOVERABLE brick. They’re rare but still a possibility so make sure you follow ALL directions EXACTLY.

    This guide will work on first-generation Switch consoles in all regions on firmware 9.2.0 or below.

    You will need one of the following in order to successfully follow this guide:

    - A USB-A to USB-C cable, and a PC
    - A USB-OTG cable, a USB-A to USB-C cable, and an Android device
		- This does not work on every android phone
    - A USB-C cable, and an Android device with a USB-C port
    - A Lightning to USB-C cable, and a jailbroken iOS device
        - This method is not covered by the guide, but you can read more about it at [this website](https://mologie.github.io/nxboot/)


    You will also need a micro SD card that is at least 128 gigabytes or larger if you plan on following this guide through the emummc path, which is safer and strongly recommended. If you must use a smaller SD card, it is possible with the sysmmc path, but strongly not recommended.

If everything goes according to plan, you will lose no data and end up with everything that you started with (games, Nintendo Account, saves, etc will be preserved).

Keep your device plugged in and charged throughout the entire process to avoid data loss or damage from an unexpected power-off.

Custom Firmware is not permanent with current methods, and will be unloaded upon rebooting the system.

It is advised that you read the entire guide from start to finish one or more times before actually running through the guide with your system.

&nbsp;

#### [Continue to Getting Started <i class="fa fa-arrow-circle-right fa-lg"></i>](user_guide/getting_started.md) 
