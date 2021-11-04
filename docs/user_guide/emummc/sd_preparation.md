# SD Preparation

We will now place the required files for the Atmosphere custom firmware and some additional homebrew files on the SD card.

Atmosphere has its own bootloader, called fusee. For the purposes of this guide we will be using Hekate instead, so that we can back up the system's NAND (internal storage) and take advantage of other advanced features in the future.

&nbsp;

!!! danger "FAT32 vs exFAT"
    Your SD card will need to be formatted as either FAT32 or exFAT. FAT32 is recommended as it is more stable and will work out of the box with the Switch's operating system, but has a file size limit of 4GB. If you plan on using exFAT, you will need to install the exFAT update for your Switch, which is downloaded when you insert an exFAT formatted SD card in to your Switch. Note that this will update your console and requires an internet connection.
	I recommend FAT32 because I read about too many data loss from the CFW users.  There are two ways to format your sd card as fat32, use [guiformat](http://ridgecrop.co.uk/index.htm?guiformat.htm)


!!! warning "File name extensions"
    If you use Windows, you should enable file name extensions before continuing. See [this link](../../extras/showing_file_extensions.md) for a guide on how to do this.

&nbsp;

### What you need

!!! tip ""
    - The latest release of <a href="https://github.com/CTCaer/Hekate/releases/" target="_blank">Hekate</a> (Download the `hekate_ctcaer_(version).zip` release of hekate)
    - The hekate config file: <a href="../../../files/emu/hekate_ipl.ini" download>hekate_ipl.ini</a>
    - The 90dns DNS redirection config: <a href="../../../files/emummc.txt" download>emummc.txt</a> (Optional) (Best to use this, if you do not want to play online in CFW) (It will block normal online play)
    - The latest release of <a href="https://github.com/Atmosphere-NX/Atmosphere/releases" target="_blank">Atmosphere</a> (Download the `atmosphere-(version)-master-(version)+hbl-(version)+hbmenu-(version).zip` release of Atmosphere.)
    - The latest release of <a href="https://github.com/Atmosphere-NX/Atmosphere/releases" target="_blank">fusee.bin payload for launching Atmosphere</a> (Download the `fusee.bin` payload of Atmosphere.)
    - The latest release of <a href="https://github.com/shchmue/Lockpick_RCM/releases" target="_blank">Lockpick_RCM</a> (Download the `Lockpick_RCM.bin` release of Lockpick)
    - The latest release of <a href="https://github.com/J-D-K/JKSV/releases" target="_blank">JKSV</a> (Download the `JKSV.nro` release of JKSV)
    - The latest release of <a href="https://github.com/mtheall/ftpd/releases" target="_blank">FTPD</a> (Download the `ftpd.nro` release of FTPD)
    - The latest release of <a href="https://github.com/exelix11/SwitchThemeInjector/releases" target="_blank">NXThemeInstaller</a> (Download the `NxThemesInstaller.nro` release of NxThemeInstaller)
    - The latest release of <a href="https://github.com/joel16/NX-Shell/releases" target="_blank">NX-Shell</a> (Download the `NX-Shell.nro` release of nx-shell)
    - The latest release of the <a href="https://github.com/vgmoose/hb-appstore/releases" target="_blank">hbappstore</a> (Download the `appstore.nro` release of hbappstore)

### Instructions

!!! tip ""
    1. Insert your Switch's SD card into your PC
    2. Copy *the contents of* the Atmosphere `.zip` file to the root of your SD card
    3. Copy the `bootloader` folder from the Hekate `.zip` file to the root of your SD card
    4. Copy `hekate_ipl.ini` to the `bootloader` folder on your SD card
    5. Copy `Lockpick_RCM.bin` and `fusee.bin` to the `/bootloader/payloads` folder on your SD card
    6. Create a folder named `hosts` inside the `atmosphere` folder on your SD card, and put `emummc.txt` in it. (Optional) (Best to use this, if you do not want to play online in CFW) (It will block normal online play)
    7. Create a folder named `appstore` inside the `switch` folder on your SD card, and put `appstore.nro` in it
    8. Copy `JKSV.nro`, `ftpd.nro`, `NX-Shell.nro` and `NxThemesInstaller.nro` to the `switch` folder on your SD card
    9. if you have Nintendo folder, copy to the root of your microSD card then you need to copy the contents of the Nintendo folder from the root of the sd card to the emummc/RAW1/Nintendo folder
    10. Reinsert your SD card back into your Switch

     ![sdfilesimg](../img/sdfiles.png)

!!! note "Restoring your existing Nintendo folder"
     If you were already using your microSD card as a storage device for your games and backed it up before partitioning your microSD card, it is now safe to restore it. Place it back on the root of your microSD card.   
	 
	 if you want same games on emuMMC, you need to copy the contents of the Nintendo folder from the root of the sd card to the emummc/RAW1/Nintendo folder.    

&nbsp;

#### [Continue to Entering RCM <i class="fa fa-arrow-circle-right fa-lg"></i>](entering_rcm.md)
