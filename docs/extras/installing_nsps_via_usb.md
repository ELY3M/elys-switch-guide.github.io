# Installing nsps over USB with goldleaf + Quark




!!! warning "Installing homebrew nsps will lead to the console ban!"
	you need to make sure you are using emunand offline or with incoginto enabled, to prevent ban on your sysnand.      
	if your console is already banned, just ignore this warning :)  



Goldleaf is multipurpose homebrew tool for Nintendo Switch.   
More info about Goldleaf is at [https://github.com/XorTroll/Goldleaf](https://github.com/XorTroll/Goldleaf)   

Quark.jar is a PC tool, with a fancy UI and made in Java, in order to help Goldleaf with the remote PC option. It should work on Windows, Linux or Mac.   
Only requirement for Quark to work is Java 9 or above in Windows (or a very simple one) is to install [AdoptOpenJDK 11 or higher](https://adoptopenjdk.net).   
Right now, I am using Java JDK 13 from [https://www.oracle.com/technetwork/java/javase/downloads/jdk13-downloads-5672538.html](https://www.oracle.com/technetwork/java/javase/downloads/jdk13-downloads-5672538.html)


!!! tips "you need sigpatches installed on your CFW.  go to [sigpatches](/extras/sigpatches) for instructions on installing the sigpatches.  "

##One time setup

1. install the sigpatches, you have not installed them before.  Read [here](/extras/sigpatches) for instructions on installing the sigpatches.  
2. Download latest Goldleaf.nro and Quark.jar from [here](https://github.com/XorTroll/Goldleaf/releases)
3. on your switch sd card, Make Goldleaf folder in /switch folder and put Goldleaf.nro in the Goldleaf folder in /switch folder.   
4. put Quark.jar in your preferred place on your computer.   
5. if you do not have JAVA JRE installed on your computer, Download Java JRE from [here](https://www.oracle.com/technetwork/java/javase/downloads/jre8-downloads-2133155.html)
6. Install Java JRE on your computer. 
7. Download Zadig from here [here](https://zadig.akeo.ie/)  
8. Open Goldleaf and connect your Switch via USB with your PC  
9. Open Zadig  
10. Click "Options" and select "List all devices"  
11. Select the Switch from the drop-down menu  
12. Change the driver (right next to the green arrow) to "libusbK"  
13. Click on the button below "Install WCID Driver" or "Replace Driver"  
14. Done. Now you can use Goldleaf and Quark to directly access your PC!  


Note: To use it correctly, make sure you open Goldleaf and connect the Switch with your PC before you launch Quark. Nevertheless, Quark will warn when USB connection is gone or no USB connection is found.



       
&nbsp;
