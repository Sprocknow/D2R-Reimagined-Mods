# How To Mod Diablo 2 Resurrected Re-Imagined

This repository contains tools and guides relevant to modding Diablo 2 Resurrected Re-Imagined.

#### Specific Guides



**Creating New Stash Tabs in Diablo 2 Resurrected:**

********* NOT MY VIDEO CREDIT TO ORIGINAL CREATOR: HighTechLowIQ **********

[![Adding New Stash Tabs in Diablo 2 Resurrected](https://img.youtube.com/vi/rAsr9Zvmn_Q/0.jpg)](https://www.youtube.com/watch?v=rAsr9Zvmn_Q)

This video looks at how to make a bigger stash in D2R by adding new shared stash tabs. It involves editing the bankexpansionlayouthd.json, using SpriteEdit to create new stash tabs, and then hex editing the SharedStashSoftCoreV2.d2i.

The modded files from HighTechLowIQ shown in this video can be found in HighTechLowIQ's repository, [Here](https://github.com/HighTechLowIQ/ModdingDiablo2Resurrected/blob/master/mods/stashtabs.mpq)

My Files for 142 Pixel and 180 Pixel Tabs Can be found in my repository here:
[142 Pixel](https://github.com/Sprocknow/D2R-Reimagined-Mods/tree/main/stash142pix)
[180 Pixel](https://github.com/Sprocknow/D2R-Reimagined-Mods/tree/main/stash180pix)

***Credit to the 180 pixel sprite modification to Can of Soup from the discord***



**Changing the Duration of Assassin Charges [Default of 15s]:**


## Text Guide

First up we need to modify the file "bankexpansionlayouthd.json" location should be in:

\Your D2R install Location\mods\Merged\Merged.mpq\data\global\excel

![FileLocation](https://github.com/user-attachments/assets/99e6669f-b5a1-4584-ac71-e50f78829a9b)

You will want to edit the file to look like the imagine below for 180 Pixels wide tabs and 8 Tabs total:

Note: If you want to rename your tabs you can, just remove the @shared, and rename them as shown in my imagine to whatever you want, you must leave the second tab as @shared though or it will cause issues..

By default for 8 tabs, that line will be:

"textStrings": [ "@personal", "@shared", "@shared", "@shared", "@shared", "@shared", "@shared", "@shared"],

Make sure to change tab count to 8, and change the tabsize to 180 for 8 tabs

![Filefor8Tabs](https://github.com/user-attachments/assets/3f8ba3b5-9df2-462e-8272-f909982577fb)

if you want to do 6-7 tabs just enter the corresponding numbers and use the 142 pixel sprite, i imagine the 180 pixel sprite will work just fine for less tabs aswell, i have not tested that.

Next Up you want to replace the stash folder in the location shown below with the files from my repository [Here](https://github.com/Sprocknow/D2R-Reimagined-Mods/tree/main/stash180pix) Or [Here if 142 Pixel](https://github.com/Sprocknow/D2R-Reimagined-Mods/tree/main/stash142pix)

\Your D2R Install Location\mods\Merged\Merged.mpq\data\hd\global\ui\panel\

![LocationforStashSprites](https://github.com/user-attachments/assets/c9dd5a36-1029-428a-bed6-077d960def3a)

Last up is we need to Hex edit the shared stash file.



## Tools

1. [SpriteEdit](https://github.com/eezstreet/D2RModding-SpriteEdit/releases)
2. [Unity D2R Scene Editor](https://github.com/pairofdocs/Unity-D2R-Scene-Editor)
3. [DS1Edit](http://paul.siramy.free.fr/_divers/ds1/dl_ds1edit.html)
4. [CascView](https://www.hiveworkshop.com/threads/ladiks-casc-viewer.331540/)
5. [Hex Editor](https://hexed.it/)

## Links
