---
title: How To Emulate Pinta's Quest For Dreamcast's Skies Of Arcadia
date: 2025-03-17 01:51 -0400
category: Gaming
tags: [Dreamcast, Sega, Skies Of Arcadia, Overworks]
description: With some (relatively) modern tools, you can experience the VMU-only activity for yourself!
image: assets/img/ElysianVMU_3uSRb4knyj.png
---

While there have been numerous ways to get the VMU activity working physically even to this day, those who're stuck with emulation have been unable to tap into it for some time now. With a bit of elbow grease, however, it's possible to not only play it, but it'll also be possible to transfer the gold and items you've accumulated from it as well!

## Step 0. Preparations

Here's what you will need
 - [Flycast](https://flyinghead.github.io/flycast-builds/) or [Redream](https://redream.io/)
 - [VMU Explorer](https://segaretro.org/VMU_Explorer)
 - [ElysianVMU](https://github.com/gyrovorbis/libevmu)

> Although I tested to ensure both emulators are able to work for this, I recommend Flycast over Redream. It's more active in development, and is auto-configured to run the Dreamcast Live servers!
{: .prompt-info }

## Step 1. Getting The Files

First, launch Skies Of Arcadia. Once you're able to activate the Pinta's Quest activity, open the Menu (whichever button you've marked the Dreamcast's X input on), then hit Next Page. Select the Pinta Quest option once you're there.

![SoA Pinta Quest option hovered over](assets/img/Flycast-2025-03-17 13-44-40.png){: w="1425" h="1069" }

> Goes without saying, but make sure you have enough space to ensure it'll actually save! The file takes up 83 of the VMU's 200 blocks. If necessary, select the BIOS from Flycast's main menu (or Saves in Redream's case), go towards the File icon, and delete anything unnecessary.
{: .prompt-tip }

Once inside, select the Dispatch option. This will save a data file to housing the titular activity. You *may* need to press A twice to get it to save.

![Pinta Quest Dispatch ask](assets/img/flycast_BrVrpFyGq2.jpg)
![Pinta Quest Dispatch confirmation](assets/img/flycast_w0aRK6eE6G.jpg)

## Step 2. Setting Up Exports

Open the VMU Explorer, then navigate to the folder containing your VMU files (for Readream, this should be in the Root, and for Flycast, in Data). For clarification, the PQ data I'll be using from hereon is one I've already been working on prior to making this guide.

![Flycast VMU Location](/assets/img/vmuexplorer_kcVwUkpkv3.png) 
_Image showcasing my Flycast's data folder and its contents_
![Redream VMU Location](/assets/img/redream%20vmu%20location.png){: w="768" h="359" }
_Image showcasing my Redream folder and its contents_

Once there, double-click the VMU bin that contains the Pinta's Quest data (in my case, vmu_save_A1.bin).

![VMU Explorer of vmu_save_A1.bin](/assets/img/vmuexplorer_lNQZuCvOkG.png)
_The VMU Explorer program window, showcasing all of the items within it._

Hover over, then right-click, on S.ARCADIA_VM, AKA the one with the Arcadia VMUgame descriptor. Once the menu pops up, select Export, then save under the .VMI/VMS or .DCI format. Both will work, but I've had far greater consistency with the latter.

![Exporting S.ARCADI](/assets/img/5x0EoN3vm1.png){: w="700" h="400" }

Once you've confirmed that the file has been exported properly, delete the one in the Explorer. We'll need the space for an import afterwards. Go to File -> Save VM to keep the changes, then exit the program.

## Step 3. Playing, Then Importing

Open ElysianVMU, then drag over the file you've just exported onto it. Once that's done, two windows will open up: the main game window, and another for file management. From here, you can play for however long you want - you don't even need to keep the window focused, it'll allow for background inputs!

![Dodging Rocks](assets/img/ElysianVMU_PkNUCFSzbe.png)
![Trading](assets/img/ElysianVMU_Qdub5VPe6e.png)
![PRESS BUTTONS QUICKLY](assets/img/ElysianVMU_oih4yb0YJs.png)

After you've had your fill of it, go over to EVMU's other window, right-click on the only file there, then click Export once again. As mentioned prior, both formats work, but I've had consistent success with .DCI. When asking for where to save, place it somewhere else on your computer, **<ins>not</ins>** in the same location from before. 

![Exporting from ElysianVMU](assets/img/ElysianVMU_Q8MwlIxDx1.png)

Open up VMU Explorer once again, and select the same VMU bin you used beforehand. Once there (and after making sure you deleted the first S.ARCADIA_VM file!), go to File -> Import File, then select the file you've just exported from ElysianVMU.

![Import VMUE](assets/img/LbcTt3pucj.png){: w="500" h="350" }

Afterwords, go to File -> Save VM once again, saving the import job, and exit. Once that's done, open up Skies Of Arcadia again with the emu you've been working the VMU files on. Load a save - preferably the latest file - then go back to the Pinta's Quest option in the menu again. You will now see a selection called Return. Activate it, and all the progress you've done on that VMU activity will successfully transfer over to your main game. Once that's done, it'll make *another* data file onto the VMU, allowing you to continue the process throughout your adventure in the game!

![Pinta's Quest Return Option](assets/img/Flycast-2025-03-17 15-20-08.png){: w="1425" h="1069" }
![Pinta's Quest Results](assets/img/Flycast-2025-03-17 15-20-37.png){: w="1425" h="1069" }
![Pinta's Quest Results 2](assets/img/Flycast-2025-03-17 15-20-41.png){: w="1425" h="1069" }
![Pinta's Quest Results 3](assets/img/Flycast-2025-03-17 15-20-45.png){: w="1425" h="1069" }

## Addenda

- When playing, the inputs will be Xbox's A/Playstation's X for cancel, and B/O for confirm/status menu, and require a *slightly* harder button press for it to register. I don't have a lot of third-party controller such as 8BitDo, so unfortunately I cannot relay which of those buttons are what.
- If you're looking to get more out of the activity, check out [slodeth's GameFAQs page](https://gamefaqs.gamespot.com/dreamcast/197237-skies-of-arcadia/faqs/9894) for an overview of what's available, as well as [Eso Arcadia's page on it](https://tinyurl.com/bd2m8se7) for further elaboration, as well as what Item C, B, and A are able to net you.
- For the Headwind minigame, it's a lot easier if you "roll", IE hovering then rhythmically moving your thumb up/down, between the two buttons then mashing simultaneously. I've gotten the bar to the top numerous times this way!

> When exporting from ElysianVMU sure the file size of each VM data matches the one below. **Very** rarely it will output one of a lower file size, and can't be registered by VMUE. If that happens, try the VMUE export file again, mess around for a bit and it'll save properly then.
{: .prompt-warning }

![File Size](assets/img/explorer_jihzVQa6ZY.png){: w="700" h="400" }