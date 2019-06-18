
# HelloBox 8 upgrade introduction
## usb upgrade
1. download the latest hellobox 8 firmware from [www.freedvb.com](http://www.freedvb.com)
2. below take the firmware `hellobox8_20190617.bin` as an example
3. put the firmware `hellobox8_20190617.bin` in the USB root directory, insert the USB to the box 
4. goto Mainmenu -> tools -> USB upgrade menu
5. select the firmware `hellobox8_20190617.bin` in *Upgrade file* field
6. select "YES" option in *Save data* field if you want save the programs/user settings/accounts, select "NO" if you want a clean new firmware
7. press OK on *Start*, and the upgrading process will start
8. wait the process to finish, it will reboot automatically

```
exceptions:
it will popup "**Upgrade fail**" if your firmware is not for Hellobox 8.
```

## usb dump
1. goto Mainmenu -> tools -> USB upgrade menu
2. press RED key to dump current firmware(including all your programs/user settings/..) to USB
3. notice the red prompt in the menu bottom for dump file name.

## network upgrade
1. prompt "New version found" will show if there is new hellobox 8 firmware version released
2. connect the network correctly, and goto Mainmenu -> tools -> Network upgrade menu
3. select "YES" option in *Save data* field if you want save the programs/user settings/accounts, select "NO" if you want a clean new firmware
4. press OK on *Start*, and the box will check the version information on the server
5. version information about current box version and the latest stable version on the server will be prompted, and select YES if you want to upgrade
6. wait the process to finish, it will reboot automatically

```
exceptions:
	it will popup "**Upgrade fail**" if the box can not get version information or box firmware on the server
	it also fails if the firmware is broken after finishing downloading
```

## exception handle
> for some unexpected reason, your hellobox 8 may crash, and can not boot up correctly. Do not be panic, check this:
**power on the box and check if the panel LED can display "boot" or not**

1. if the front panel LED can display "boot", it's fine, please use **auto upgrade** 
2. if no front panel LED display at all :(, the only way is using **RS232 upgrade**

### auto upgrade
1. power off the box
2. rename the firmware to `auto_burn.fac`, and put it in the USB root directory
3. insert the USB to the box, and power on the box
4. if the USB is correctly detected, it will display "USB" for about 5~10 seconds, and start to upgrade automatically, and the panel will show the progress "U0xx"
5. it will show "FFFF" after finishing. 
6. REMOVE THE USB AND DELETE THE "auto_burn.fac" FILE IN USB!!!
7. power on the box, it will be back

```
exceptions:
	if step 4 not work, please try another USB. As known, some USB does not work well under this condation.
```

### RS232 upgrade
this is the final way to recovery the box. it need you to open the box and connect the RS232 cable to PC.
1. first remove the screw under the box
![remove the screw](screw.jpg)


