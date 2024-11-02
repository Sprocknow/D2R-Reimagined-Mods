# How To Mod Diablo 2 Resurrected Re-Imagined

This repository contains tools and guides relevant to modding Diablo 2 Resurrected Re-Imagined.

#### Specific Guides

Reference for modifying the stash for clean D2R

**Creating New Stash Tabs in Diablo 2 Resurrected:**

********* NOT MY VIDEO CREDIT TO ORIGINAL CREATOR: HighTechLowIQ **********

[![Adding New Stash Tabs in Diablo 2 Resurrected](https://img.youtube.com/vi/rAsr9Zvmn_Q/0.jpg)](https://www.youtube.com/watch?v=rAsr9Zvmn_Q)

This video looks at how to make a bigger stash in D2R by adding new shared stash tabs. It involves editing the bankexpansionlayouthd.json, using SpriteEdit to create new stash tabs, and then hex editing the SharedStashSoftCoreV2.d2i.

The modded files from HighTechLowIQ shown in this video can be found in HighTechLowIQ's repository, [Here](https://github.com/HighTechLowIQ/ModdingDiablo2Resurrected/blob/master/mods/stashtabs.mpq)


My Files for 142 Pixel and 180 Pixel Tabs Can be found in my repository here:
[142 Pixel](https://github.com/Sprocknow/D2R-Reimagined-Mods/tree/main/stash142pix)
[180 Pixel](https://github.com/Sprocknow/D2R-Reimagined-Mods/tree/main/stash180pix)

***Credit to the 180 pixel sprite modification to Can of Soup from the discord***


## Text Guide

**Creating New Stash Tabs in Diablo 2 Resurrected: Re-Imagined Mod**

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

Last up is we need to Hex edit the shared stash file which is in the folder shown below using a [Hex Editor](https://hexed.it/):

your D2R drive location:\Users\Your User name\Saved Games\Diablo II Resurrected\mods\Merged

![Sharedstashlocation](https://github.com/user-attachments/assets/425f33a7-b3cd-4306-98a8-cab582571223)

Open the [Hex Editor](https://hexed.it/) and Load the file in the location shown above

This works best with a FRESH Mod install and no items in any previous stash tabs

![FreshStashFileEMPTYSTASH](https://github.com/user-attachments/assets/7f8f74eb-23d1-4288-86ec-1225e942cd99)

You can see the code shown for the stash tabs here [For Empty tabs] Repeats 3 times as shown below:

![RepeatedCode](https://github.com/user-attachments/assets/54766945-16f5-4fb0-8738-46c1c54ff010)

You want to highlight the code that repeats and then go to the + at the end of the hex file, right click and select Insert selected bytes here:

![InsertBytesHere](https://github.com/user-attachments/assets/ec7c7489-36bd-496e-8565-756dcf6f46fe)

You want to paste the section of bytes so theres 7 total repeating sections [for a total of 8 tabs, which includes your one personal tab]

The personal tab does not show in this file, so there will be 7 repeated codes.

![PastedBytes7times](https://github.com/user-attachments/assets/7d7c4631-dd27-45d6-bf48-fa6d774b61c0)

Save the file, and go load up D2R Re-Imagined and enjoy the extra tabs!

Note:  This CAN be done on a used mod install, but the hex editing will be VERY different and considerbly more difficult. The stash file will be absolutely massive, the the code is NOT REPEATING because its based on the items you have in the stash. I HIGHLY recommend fully emptying the stash out and backing up your entire Merged folder before you attempt modifying an existing mod install for more tabs. But it can be done. Use Care and back up everything as mentioned.


**Changing the Duration of Assassin Charges [Default of 15s]:**


To change the duration of the Assassin Charges you need to edit the skills.txt in the location shown below:

Install Drive:\D2R Install Folder\mods\Merged\Merged.mpq\data\global\excel

![2024-11-02 (3)](https://github.com/user-attachments/assets/f2def6f2-badb-4b8f-b607-e7cdea5cd5fc)

Look for your Assassin Skill names to change the durations: Cobra Strike, Blades of Ice, Claws of Thunder, etc...

![2024-11-02 (1)](https://github.com/user-attachments/assets/92abebc5-3496-417b-9b6a-c013ef5123f5)

if you highlight the line, then move the scroll bar to the right, eventually youll see " Duration 375 "  Which is 375 frames or 15 seconds which is the default

I made Mine 800 frames, which is rouhgly 30 seconds, or double, you can change the value to whatever you want, 1 second is 25 frames for reference.

![2024-11-02 (2)](https://github.com/user-attachments/assets/80e72eac-c874-47db-9721-539cf36a7306)

Phoenix Strike is Called Royal Strike in the skills file however, and the duration is closer to the left, without the work Duration in front of it, as shown below.

![2024-11-02](https://github.com/user-attachments/assets/29f9a35d-5965-4804-9dfc-4ac2879f72fc)

Save your file, and enjoy not having to reset your charges for as long as you choose to modify it to!







## Tools

1. [SpriteEdit](https://github.com/eezstreet/D2RModding-SpriteEdit/releases)
2. [Unity D2R Scene Editor](https://github.com/pairofdocs/Unity-D2R-Scene-Editor)
3. [DS1Edit](http://paul.siramy.free.fr/_divers/ds1/dl_ds1edit.html)
4. [CascView](https://www.hiveworkshop.com/threads/ladiks-casc-viewer.331540/)
5. [Hex Editor](https://hexed.it/)

## Links
