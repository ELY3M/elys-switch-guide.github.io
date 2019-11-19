# Atmosphere Tips 


<font size=6>changing how you launch hbmenu and games</font><p>





This is the default loader.ini config in /atmosphere/
<pre>
[hbl_config]
title_id=010000000000100D
override_any_app=true
path=atmosphere/hbl.nsp
override_key=R

[default_config]
override_key=!L
cheat_enable_key=!L
</pre>
<p>


I started with atmosphere 0.8.3 that I normally tap on album icon to open my hbmenu and tap on games to open games.  
When I updated to 0.8.5, I open my album to see my own gallery of pics like in OFW.  I read thru change logs on the github.  
I had to press R to open hbmenu from my album.  I open games to see hbmenu.  I would have to press R to open one of games to game.  
<p>
I decided to make it abit easier by editng my loader.ini  
I added ! before R in this line override_key=R
making this line to be override_key=!R   
<p>
next thing, when I open one of my games, it go to hbmenu.  
I figured out that it will help me to get full RAM for retroarch or other homebrew apps.    
I decided to leave it to true because I run retroarch.  
<p>
I know some people do not need full RAM.   
if you do not need full RAM, you can change this line 
override_any_app=true to override_any_app=false
so you do not have to hold R when opening your game.   


<p><br>


My own loader.ini here<p>

<pre>
[hbl_config]
title_id=010000000000100D
override_any_app=true
path=atmosphere/hbl.nsp
override_key=!R

[default_config]
override_key=!L
cheat_enable_key=!L
</pre>

<p>

<br><br><br>


<font size=6>Disabling Cheats</font><p>

Atomsphere come with cheat engine enabled on default settings.     
I saw that many people have issues with games or want cheats disabled.      
<p>
Open system_settings.ini in atmosphere folder and find this line 
<p>
dmnt_cheats_enabled_by_default = u8!0x1
<p>
change this line to <p>
dmnt_cheats_enabled_by_default = u8!0x0

<p>
If you want to cheat. you have to leave it as u8!0x1 
<p>
More info on cheating here: <a href=cheating.html>My Cheating Tutorial</a>
<p>

<br><br><br>

<font size=6>Custom Boot Screens</font><p>


I read thru gbatemp and found out that people are able to make custom boot splash screen.  
very cool!    <p>

The custom boot splash screen have to be 1280 x 720 and rotated 90 counterwise.  
It can be done easily in photoshop and saved as a bmp in 32bit.   
<p>
More of the splash screens and more of my made ones too. <br>
<a href=https://github.com/ELY3M/Atmosphere-Splashes/>Atmosphere Splashes</a>
<p>
I add this line to BCT.ini in /atmosphere/ on my sd card.   
then I put bootlogo.bmp in the atomosphere folder.
<pre>
[stage2]
custom_splash = atmosphere/bootlogo.bmp
</pre>


Here is my custom boot splash screen <p>
<img src=/extras/img/splash3.png>




<p>
My own BCT.ini here<p>
<pre>
BCT0
[stage1]
stage2_path = atmosphere/fusee-secondary.bin
stage2_addr = 0xF0000000
stage2_entrypoint = 0xF0000000

[stage2]
custom_splash = atmosphere/bootlogo.bmp

[exosphere]
; Note: Disabling debugmode will cause parts of ams.tma to not work, in the future.
debugmode = 1 
debugmode_user = 0

[stratosphere]
nogc = 0
; To force-enable nogc, add nogc = 1
; To force-disable nogc, add nogc = 0
</pre>


After 9.0.0 update:  I have issues reading my game carts. 
after talking with ReSwitched Team.   
in the stratosphere section.  
I needed to add this nogc = 0

<pre>
[stratosphere]
nogc = 0
; To force-enable nogc, add nogc = 1
; To force-disable nogc, add nogc = 0
</pre>
       
&nbsp;
