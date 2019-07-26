
# HelloMenu_GUI Tutorial
## Introduction
HelloMenu_GUI is the customized tool for Hellobox 8. With HelloMenu_GUI, you can make your personal menu style for Hellobox 8 with convinience.
It supports:
1. export/import the blocks in the firmware
2. export/import the icons/strings/font in the firmware
3. configuration for default language, menu style colors, and so on
```
Notice:
The firmware before 20190725 does not support configuration function!!
```

## Usage
- ### Start:
1. Download the lateste firmware from [www.freedvb.com](http://www.freedvb.com)
2. Double click the HelloMenu_GUI.exe to start the application.
3. Select the firmware from your pc  
![image](https://github.com/DVBFinder/hellobox8/blob/master/pic/hm_boot.PNG)
```
It will refuse the firmware that is not for Hellobox
```

- ### blocks:
1. Left click to select one block
2. Click the "Export" button, assign a file name, and export the selected block
3. Click the "Import" button，select a file, and replace the selected block  
![image](https://github.com/DVBFinder/hellobox8/blob/master/pic/hm_block.PNG)
```
Block 94 96 97 is the mainmenu background. 
These 3 blocks can be exported to  .jpg file, and the import file for these 3 block should also be .jpg.
Notice: pixel size: 1280*720, the recommended file size is less than 200K.

Block 93 is the bootup logo, must be .jpg file, pixel size: 1920*1080. 
The recommended file size is less than 200K.

Other blocks are not recommended to replace unless you know what are you doing. 
```

- ### Resources:
1. Click "Browse" in "Export" line to select a directory to store the exported resource
2. Select "Bitmap/String/Font/All" option to select one or all resources, and the click "Export"
![image](https://github.com/DVBFinder/hellobox8/blob/master/pic/hm_rsc.PNG) 

The export result is like this:  

![image](https://github.com/DVBFinder/hellobox8/blob/master/pic/hm_export.PNG)  
```
The exported resource files are like BITMAP_xxx.bmp, STRING_xxx.txt, FONT_XXX.ttf.
Here the xxx is the resource id.
```
3.  Click "Browse" in "Import" line to select a directory which has the resources you want to replace
4. Click the "Import" button to replace the selected resource  
![image](https://github.com/DVBFinder/hellobox8/blob/master/pic/hm_import.PNG)
```
The files in import directory should have the same name as the export directory.
For example, you want to replace the BITMAP_1 in the resource, modify the BITMAP_1 and put it in the import directory.
Same for the String: you can translate the STRING_1 to you own language, and put it as STRING_1.txt in the import directory 
```
![image](https://github.com/DVBFinder/hellobox8/blob/master/pic/hm_string.PNG)
```
!!!Important Notice:
For Bitmap, you'd better have the similar size with the original bitmap.
(170~190)*160 is recommended for the mainmenu icon
180*180 is recommended for the APP icon

For translate string, the first 3 line is very important!
the line in string_x.txt is like this:
1: Türkçe   ---> the Turkish in Turkish language, displayed in Configuration->default language
2: tur      ---> the country code 1
3: tur      ---> the country code 1

the line 2/3 is 3-letter codes for the country code, you can refer to https://www.w3.org/WAI/ER/IG/ert/iso639.htm
they can be the same if there is only one code 

For the Font, the replace .ttf file should be less than 1Mega, or it will crash(The memory is limited for embedded system)

```

- ### Configuration:
1. Select the language in the default language combo, it will update the default language  
![image](https://github.com/DVBFinder/hellobox8/blob/master/pic/hm_rsc_lang.PNG)
2. HelloMenu have 3 color style to match the corresponding mainmenu background, and you can modify the board,layer 1,layer 2, layer 3  
![image](TODO:add it later)
3. Click the button to select color you prefer  
![image](https://github.com/DVBFinder/hellobox8/blob/master/pic/hm_style.PNG)
and click 'Update' to update the color you choose.

- ### Save:
The last step is to save all your modifications!  
![image](https://github.com/DVBFinder/hellobox8/blob/master/pic/hm_save.PNG)  
Save with a new name is recommended.


## Issues
Please feel free to ask questions in [www.freedvb.com](www.freedvb.com)
