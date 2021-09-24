## Backing up your emuMMC partition on your sd card

I know some people want to backup emuMMC.          
We will be using [hekate](https://github.com/CTCaer/hekate/releases/) to both backup and restore the emuMMC, so make sure that you have its latest files on your SD card already.

### What you need:
- [Latest hekate](https://github.com/CTCaer/hekate/releases/)
- Your sd card with emuMMC partition

### Instructions:

!!!warning "Space for the backup"
    You need at least 30GB of free space to be able to backup and restore the emuMMC!

1.  Inject the hekate payload.
2.  In the main menu, tap on `Tools`, then `Backup eMMC` and set `SD emuMMC Raw Partition` at the bottom of your screen to `ON`.
3.  Backup both `SD emuMMC BOOT0 & BOOT1` and `SD emuMMC RAW GPP` (Note: raw gpp may take a while).
4.  Once both are done, go back to the main menu, remove your SD card and insert it into your PC.
5.  If Windows asks you to format a drive, discard it and select the drive with your SD contents.
6.  Copy the backup folder from your your SD card to a safe place on your PC.
7.  Put your sd card back in your switch.  


## Restoring your emuMMC partition to your sd card from the backup.  

### What you need:
- [Latest hekate](https://github.com/CTCaer/hekate/releases/)
- your backed up emuMMC files that you have saved.  
- Your sd card with emuMMC partition that you wish to restore from the backup.    
- if the sd card is new or not partitioned, make sure you follow [this guide](https://switchgui.de/switch-guide/user_guide/emummc/partitioning_sd/)
  

!!!warning "Space for the backup"
    You need at least 30GB of free space to be able to backup and restore the emuMMC!
	
1. Remove SD card from your Switch then Insert your SD card into your computer.
2. Copy your emuMMC backup folder from your pc to your sd card.
3. Navigate to `/backup/<some characters>/` on your SD card and move `BOOT0`, `BOOT1` and the `rawnand.bin.xx` files to the `restore` folder.
4. Eject the SD card and insert it into your switch.
5. Inject the hekate payload.
6. Tap on `Tools`, `Restore eMMC`, set `SD emuMMC Raw Partition` at the bottom of your screen to `ON`.
7. Restore the backup by tapping on both `SD emuMMC BOOT0 & BOOT1` and `SD emuMMC RAW GPP` (Note: raw gpp may take a while).
    - It is very important that for both of these the `SD emuMMC Raw Partition` option is enabled, otherwise you will be altering your sysMMC
      which is not what you want.
8. Make sure you have latest atmosphere files on your sd card.   
9. Your emuMMC is now restored on the SD card and you should be able to launch it with fusee.bin in your TegraRcmGUI or payload launcher.  


