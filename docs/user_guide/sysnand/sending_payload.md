

# Sending a Payload

!!! warning "If you were sent here directly"
    Make sure you've [put your device into RCM](entering_rcm.md), and downloaded Hekate (extract its zip file if necessary) before continuing.

Now that the device is in RCM, we will need to send it a payload. The methods are mostly the same, but slightly differs depending on what hardware you have available.

&nbsp;

## Windows

### What you need

!!! tip ""
    - The latest release of <a href="https://github.com/ELY3M/TegraRcmGUI---modded-by-ELY-M/releases" target="_blank">TegraRcmGUI</a> (portable zip)
    - The latest release of <a href="https://github.com/CTCaer/hekate/releases/" target="_blank">Hekate</a> (either the hekate_ctcaer bin or the hekate_ctcaer zip)
	- The latest release of <a href="https://github.com/Atmosphere-NX/Atmosphere/releases" target="_blank">fusee-primary.bin</a> from  <a href="https://github.com/Atmosphere-NX/Atmosphere/releases" target="_blank">Atmosphere</a> 
    - A USB-A to USB-C cable (or a standard USB-C cable if your computer natively supports USB-C)

### Instructions

!!! tip ""
    1. Install TegraRcmGUI by unzipping and put the contents in your preferred place on your computer.
	2. TegraRcmGUI came with the payloads in the favorites folder.  We need to make sure we update them with latest payload bins.  
		- copy the latest payload bins into the favorites folder and just say yes to overwrite.  
    3. Navigate to the `Settings` tab, then press `Install Driver` and follow the on-screen instructions
    4. Connect your Switch in RCM to your PC using the USB cable
    5. Navigate to the `Payload` tab of TegraRcmGUI 
    - Your Switch should be shown as detected in the bottom left corner
    6. Press the file button next to `Inject payload`, and navigate to and select your hekate_ctcaer `.bin` file
    7. Click `Inject payload` to launch Hekate

&nbsp;

## Mac / Linux

### What you need

!!! tip ""
    - The latest release of <a href="https://github.com/nh-server/fusee-interfacee-tk/releases" target="_blank">fusee-interfacee-tk</a>
    - The latest release of <a href="https://github.com/CTCaer/hekate/releases/" target="_blank">Hekate</a> (either the hekate_ctcaer bin or the hekate_ctcaer zip)
	- The latest release of <a href="https://github.com/Atmosphere-NX/Atmosphere/releases" target="_blank">fusee-primary.bin</a> from  <a href="https://github.com/Atmosphere-NX/Atmosphere/releases" target="_blank">Atmosphere</a> 
    - A USB-A to USB-C cable (or a standard USB-C cable if your computer natively supports USB-C)

### Instructions

!!! tip ""
    1. Download and run the payload injector (if you are on Linux, you will need to run this program as root or use `sudo`.)
    2. Connect your Switch in RCM to your PC using the USB cable
    3. Wait for your Switch to be shown as found in the injector
    4. Press `Select Payload`, and navigate to and select your hekate_ctcaer `.bin` file
    5. Click `Send Payload!` to launch Hekate

&nbsp;

## Android

### What you need

!!! tip ""
    - The latest release of <a href="https://github.com/ELY3M/Rekado---modded-by-ELY-M/releases" target="_blank">Rekado Modded by ELY M.</a>
        - You will need to enable Unknown Sources in your device settings to install this
    - The latest release of <a href="https://github.com/CTCaer/hekate/releases/" target="_blank">Hekate</a> (either the hekate_ctcaer bin or the hekate_ctcaer zip)
    - The latest release of <a href="https://github.com/Atmosphere-NX/Atmosphere/releases" target="_blank">fusee-primary.bin</a> from  <a href="https://github.com/Atmosphere-NX/Atmosphere/releases" target="_blank">Atmosphere</a> 
    - A USB-C cable
        - If your device has a USB-C port, you may use a C-C cable
        - If your device only has a Micro USB port, you will need a USB OTG adapter and a USB A-C cable
            - This **will not work** on every phone!
		
### Instructions

!!! tip ""
    1. Copy the hekate_ctcaer `.bin` file from the Hekate `.zip` file and fusee-primary.bin to a location on your phone
    - A tool such as Amaze File Manager can do this
    2. Launch Rekado on your phone
    3. Navigate to `Payloads`, then press the `+` button at the bottom right
    4. Navigate to your hekate_ctcaer `.bin` file, and tap it to add it to Rekado's menu
    5. **Optional, but recommended**: Navigate to Rekado's settings and enable `Hide bundled`
    6. Connect your Switch in RCM to your phone using the USB cable
    7. If prompted, grant Rekado access to the Switch
    8. Select your hekate_ctcaer `.bin` file in the dialog that pops up

&nbsp;

!!! danger "If nothing happens after you send the payload"
    If your console's screen remains black after you've sent Hekate, it's possible your payload was corrupted, or that your console is patched. If your payload injector program shows that 0 bytes were sent, then it is definitely patched, so you'll be unable to proceed with the rest of the guide.

&nbsp;

#### [Continue to Making Essential Backups <i class="fa fa-arrow-circle-right fa-lg"></i>](making_essential_backups.md)
