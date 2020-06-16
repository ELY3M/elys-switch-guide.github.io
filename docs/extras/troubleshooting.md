# Troubleshooting 
This page is about common issues with atmosphere and situations to fix them.   

# your game cartridges do not work or won't be read in atmosphere. 
I put in my game cart and I get error reading the game cart. 
This is because of game cart efuses (Lotus Firmware)  
it get burnt no matter even you try to avoid burning efuses.    
  
You need to add ncgc = 0 in bottom of BCT.ini in /atmosphere/config   

1. go on your sd card by ftpd method or in your computer.  
2. go to /atmosphere/config
3. open BCT.ini with notepad or your favorite text editor. 
4. go down to [stratosphere] and add nogc = 0 after [stratosphere]    
5. save the BCT.ini and if your sd card is in computer, put it back in switch.  
6. reboot switch via reboot to payload or inject fusee-primary.bin payload.    

your BCT.ini should look like this: 

<pre>
BCT0
[stage1]
stage2_path = atmosphere/fusee-secondary.bin
stage2_mtc_path = atmosphere/fusee-mtc.bin
stage2_addr = 0xF0000000
stage2_entrypoint = 0xF0000000

[exosphere]
; Note: Disabling debugmode will cause parts of ams.tma to not work, in the future.
debugmode = 1
debugmode_user = 0
; Note: Disabling usermode exception handlers will cause atmosphere to not fail gracefully under error conditions.
; Support will not be provided to users who disable these. If you do not know what you are doing, leave them on.
disable_user_exception_handlers = 0
; Note: It's currently unknown what effects enabling the usermode PMU register access may have on official code.
enable_user_pmu_access = 0

[stratosphere]
nogc = 0 
; To force-enable nogc, add nogc = 1
; To force-disable nogc, add nogc = 0
</pre>


If you are using hekate to boot atmosphere.  you need to do change in hekate_ipl.ini  
change autonogc=1 to autonogc=0 in [config] section
if it is missing, add autonogc=0 to [config] section  
like this 

<pre>
[config]
autoboot=0
autoboot_list=0
bootwait=3
customlogo=0
verification=2
backlight=160
autohosoff=0
autonogc=0
</pre>


# My homebrew freeze or crash 

you need to hold R as you tap on one of your games to open hbmenu in full ram.   

It will help with smooth running of homebrew apps.   





# archive bits
None of my homebrew is showing up.  
atmosphere crash on boot with 
<pre>
A fatal error occurred when running Atmosphére.
Title ID: 010041544d530000
Error Desc: std::abort() called (0xffe)
</pre>  

This is usually due to an archive metadata bit used by some OS’s that Horizon simply can’t deal with. Here’s how to fix it:

1. Get your switch in RCM mode.  
2. Inject Hekate payload 
3. Tap on "Tools" on top of the hekate screen.  
4. Tap on "Archive Bit - AutoRCM" on the right bottom.  
5. Tap on "Unset archive bit" button.  This might take a while, be patient.


	   
&nbsp;



# 
