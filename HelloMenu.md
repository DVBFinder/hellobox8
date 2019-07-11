
# HelloMenu tool Usage
## Introduction
HelloMenu is the customized tool for Hellobox 8. With HelloMenu tool, you can make your personal menu style for Hellobox 8 with convinience.
It supports:
1. show the blocks in the firmware, and you can replace any of the blocks
2. show the icons/strings/font in the firmware, and you can modify any of them

## Basic Usage

HelloMenu is a command line tool, The usage of HelloMenu.exe is like this:
```
HelloMenu.exe firmware [options]
```
firmware: the firmware binary download from [www.freedvb.com](http://www.freedvb.com)  
options: option arguments, based on the functions

## Usage example

below take firmware version hellobox8_20190705.bin as example
- ##### Show the usage of HelloMenu:
```
HelloMenu.exe -h
```

- ##### show the current version:
```
HelloMenu.exe -v
```

- ##### list all the blocks in firmware:
```
HelloMenu.exe hellobox8_20190705.bin -bl
```

- ##### split all the blocks in firmware to given path:
```
HelloMenu.exe hellobox8_20190705.bin -bs target_dir
```
It will split all the block data into "target_dir" (the directory will be created if not exist). the blocks binary starts with "0xXX_", here XX is the block ID, used in block replace.

- ##### replace one or more block in firmware, format after '-br': id block_file [id block file ...]:  
replace block 94 with menu1.jpg:
```
HelloMenu.exe hellobox8_20190705.bin -br 94 menu1.jpg 97 menu2.jpg
```
replace block 94 with menu1.jpg, replace block 97 with menu2.jpg:
```
HelloMenu.exe hellobox8_20190705.bin -br 94 menu1.jpg 97 menu2.jpg
```
Here background picture should be JPEG, and image pixel 1280*720, and file size should be less than 300K
This command will generate a new modified firmware hellobox8_20190705.bin_new.bin.

- ##### extract all the resource item(bitmap/string/font) to given path:
```
HelloMenu.exe hellobox8_20190705.bin -e target_dir
```
It will extract all the resource items into "target_dir" (the directory will be created if not exist). It has BITMAP_XX.bmp, STRING_xx.txt, font.ttf

- ##### extract one or more bitmaps to current directory:
```
HelloMenu.exe hellobox8_20190705.bin -eb 193 194 195
```
extract bitmap id 193 194 195 to current directory

- ##### extract one or more string files to current directory:
```
HelloMenu.exe hellobox8_20190705.bin -bs 1 2 3
```
extract string file id 1, 2, 3  to current directory

- ##### extract font.ttf to current directory::
```
HelloMenu.exe hellobox8_20190705.bin -bf 1
```

- ##### update all the resource items in file to the firmware and generate a new firmware:
```
HelloMenu.exe hellobox8_20190705.bin -u all.txt
```

- ##### update all the resource items in file to the firmware and generate a new firmware:
```
HelloMenu.exe hellobox8_20190705.bin -u all.txt
```

- ##### update bitmaps to the firmware and generate a new firmware:
```
HelloMenu.exe hellobox8_20190705.bin -ub 193 193.jpg 194 194.png 195 195.bmp
```
The icon should have the similar size as the original one, the transparent color is (0,255,255)

- ##### update string file to the firmware and generate a new firmware:
```
HelloMenu.exe hellobox8_20190705.bin -us 1 str1.txt 2 str2.txt
```

- ##### update font file to the firmware and generate a new firmware:
```
HelloMenu.exe hellobox8_20190705.bin -uf 1 font.ttf
```

## Known limitation about the resource
- the bootlogo must be 1920*1280, JPEG
- the menu background should be 1280*720, JPEG
- the icon transparent color is RGB: (0, 255, 255)
- the icon you want to replace should have the similar size as the original one

## Future
HelloMenu is command line tool, and someone may not feel comfortable with it. The GUI version is on our schedule now, and will update it later.


