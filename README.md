
# Hellobox 8 upgrade introduction
## USB Upgrade
1. Download the latest Hellobox 8 firmware from [www.freedvb.com](http://www.freedvb.com)
2. Take the firmware `hellobox8_20190617.bin` as an example below
3. Put the firmware `hellobox8_20190617.bin` into the USB root directory, and insert the USB to the box 
4. Go to Mainmenu -> tools -> USB upgrade menu
5. Select the firmware `hellobox8_20190617.bin` in *Upgrade file* field
6. Select "Yes" option in *Save data* field if you want to save the programs/user settings/accounts, or "No" if you want a clean new firmware
7. Press OK on *Start* to start the upgrading process
8. Wait for the process to complete, it will reboot automatically

![image](https://github.com/DVBFinder/hellobox8/blob/master/pic/usb_upg.jpg)
![image](https://github.com/DVBFinder/hellobox8/blob/master/pic/usb_upg_prompt.jpg)
```
Exceptions:
It will prompt "Upgrade fail" if your firmware is not suitable for Hellobox 8.
```

## Backup firmware with USB
1. It is strongly recommended to back up the firmware before upgrading
2. Go to Mainmenu -> tools -> USB upgrade menu
3. Press RED key to dump current firmware(including all your programs/user settings/..) to USB
4. Notice the red prompt of the dump file name at the bottom of the menu
5. Backup firmware can be used to restore all your previous information

![image](https://github.com/DVBFinder/hellobox8/blob/master/pic/usb_dump.jpg)

## Network upgrade
1. If a new Hellobox 8 firmware version is released, Hellobox 8 will display "Found New Version" at startup
2. Connect to the network correctly, and go to Mainmenu -> tools -> Network upgrade menu
3. Select "Yes" option in *Save data* field if you want to save the programs/user settings/accounts, or "No" if you want a clean new firmware
4. Press OK on *Start*, then the box will check the version information on the server
5. Check the version information about current Hellobox 8 version and the latest stable version on the server, and select "Yes" if you want to upgrade
6. Wait for the process to complete, it will reboot automatically

![image](https://github.com/DVBFinder/hellobox8/blob/master/pic/net_upg.jpg)
![image](https://github.com/DVBFinder/hellobox8/blob/master/pic/net_upg_progress.jpg)

```
Exceptions:
It will prompt "Upgrade fail" if the box cannot get version information or box firmware on the server
It will also fail if the firmware is corrupted after downloading
If it takes too long to download, you can power off the box only if the progress is less than 50%. 
DO NOT POWER OFF the box if the progress is bigger than 50%!
```

## Exception handle
> For some unexpected reason, your Hellobox 8 may crash, and fail to start properly. Don't panic, check it out:
> 
**Turn on the Hellobox 8 power, and check the panel LED display**

1. If the front panel LED can display "boot" as shown below, that's fine, please follow **auto upgrade** section
![image](https://github.com/DVBFinder/hellobox8/blob/master/pic/boot.jpg)
2. If there is no front panel LED display when bootup :(, please follow  **RS232 upgrade** section

### Auto upgrade
1. Turn off the Hellobox 8 power
2. Rename the firmware to `auto_burn.fac`, and place it in the USB root directory
3. Insert the USB into Hellobox 8, and turn on the power
4. The box will display "USB" for about 5~10 seconds if the USB is detected correctly, and the upgrade process will start automatically. The panel will show the progress "U0xx"
5. When finished, "FFFF" will be displayed. 
6. REMOVE THE USB AND DELETE THE `auto_burn.fac` FILE IN USB!!! 
7. Turn off and turn on the box, it will be back

*add gif here later*
![gif of auto upgrade](https://github.com/DVBFinder/hellobox8/blob/master/pic/auto.gif)

```
exceptions:
If step 4 does not work, please try another USB. As known, some USB does not work properly in this case.
If step 6 is forgotten, the box will upgrade again and again. 
So remember to remove the "auto_burn.fac"! 
```

### RS232 upgrade 
This is the last way to recover the box. it requires you to open the box cover, and connect the RS232 cable to PC. 
1. Remove the screws under the box
2. Open the box very carefully! The WIFI antenna is connected to the box cover
3. Insert a 3-wire RS232 interface, and connect the RS232 to PC
4. Upgrade using PC tool. 

**update this section with picture later!**


