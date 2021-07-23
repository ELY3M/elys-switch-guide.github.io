# Partitioning the SD Card and making emuMMC

!!!warning "This will delete everything on your sd card"
	Doing this will delete all your data from your sd card, be warned!

!!! warning "Back up your existing Nintendo folder"
	Before we start, if you are using a microSD card already as a storage device for your games, you will want to back up your `Nintendo` folder that is on the root of your microSD card to a safe place on your computer. This folder contains your downloaded games and game updates.

-----

## Preparations

What you need:

- The latest release of <a href="https://github.com/CTCaer/hekate/releases" target="_blank">Hekate</a>

<b>NOTE:</b> We will be using Hekate to do SD partitioning for emuMMC.  Hekate now have function to do SD partitioning for formatting and SD partitioning for emuMMC

### Instructions

1. Make sure you are done with SD preparation part of this guide.   

2. Inject the Hekate payload with your 128GB (or larger) SD card inserted into your Switch.
	- If you forgot how to do this, re-read the [sending payload](sending_payload.md) section of the guide.

3. Tap on "tools" on top of the Hekate screen.  

4. Tap on "partition SD card" button   

5. When the dialog come up with your sd card info and files size. Click on OK.    

6. When the bars come up.  go for the red bar that have emuMMC (RAW): on left.  Move the toggle on right to left till it say 29 FULL on right.   

7. Tap on "Next Step" button on bottom and right.    

8. The Partition Manager Dialog will come up. it will warn you about wiping out other partitions on your sd card.  Tap on "Start" button.   

9. Hekate will backup your files on your SD card first for awhile.  Hekate will do partitioning for awhile.   

10. the dialog will come up that say It is done. Just tap on "Ok" button.  

11. go back to main Hekate screen by tap on close.  

12. on main Hekate screen, Tap on emuMMC button on right.  

13. Tap on `Create emuMMC`, then select `SD Partition`

14. Tap on `Part 1`. It will start making the emuMMC now. After it's done return to the emuMMC menu using the `Close` buttons
	
15. It will take 15 to 30 mins creating your emuMMC in the new sd partition.    


you can watch me making partition on my sd card in Hekate here.   
<iframe width="560" height="315" src="https://www.youtube.com/embed/fhQiabtZq3I" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


after the emuMMC is done, launching atmosphere.   
<iframe width="560" height="315" src="https://www.youtube.com/embed/rC4B930zIxU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>



!!! warning "Windows complaining about an unreadable drive"
    If you get the issue that Windows says the SD card is unreadable and wants to format it, do not format! This is likely your emuMMC partition. After partitioning your sd, your sd will show up as 2 drives on your pc. Use the drive that can be accessed
    
&nbsp;

#### [Continue to SD Preparations <i class="fa fa-arrow-circle-right fa-lg"></i>](sd_preparation.md)
