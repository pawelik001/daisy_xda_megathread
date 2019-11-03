Welcome all XDA users! Since most devices have something like “mega thread” for specific device, and our beloved Mi A2 Lite (daisy_sprout) doesn't have, I've decided to make one, maybe for someone who doesn't use Telegram it will be useful.

WARNING: We (creators of this post and all modifications) are not responsible for what happens to your phone! But remember, we can always do our best to help you! Happy modifications!

All guides are imported/modified/created/deleted from Telegram. 
So let's start!



CHAPTERS:
Prerequisites
Unlocking bootloader
Installing recoveries
Flashing ROM’s
Flashing kernels
Flashing GSI
Guides
Files
Others

0. Prerequisites

There you have some useful files at start
Minimal ADB and fastboot: http://forum.xda-developers.com/showthread.php?t=2317790
MiFlash for flashing stock rom: https://xiaomifirmware.com/downloads/download-latest-version-mi-flash-tool-v-7-4-25/
Nice tutorial containing almost everything written by tkchn, modified by me: https://github.com/pawelik001/daisyinstall
Brain, of course, to not ended up destroying your daisy_sprout, and to understand this thread

And useful spreadsheets, I will put here all of them, but in every chapter they will be too.
ROM’s: https://docs.google.com/spreadsheets/d/1Uy6qouIV0WbVouK4X5PhmUz2quxfLguHDqSf6LYDBO8
Kernels: https://docs.google.com/spreadsheets/d/1FnVxHI9TBeGP7tn_oRNdtSlWjMUcwwfVkbwyzO5AEj0
Recoveries: https://docs.google.com/spreadsheets/d/1zunbZBh_HoFj4iUsffqQFc3dmuBKzAGp3xku22kJqwg
Files: https://docs.google.com/spreadsheets/d/1I1XPH3LjLmlyDED3YJM0Sqp-wTIEqM3uKeUwWx8VPxs

1. Unlocking bootloader

WARNING: 
THIS WILL VOID YOUR WARRANTY
BE SURE TO BACK UP YOUR INTERNAL STORAGE, AS THIS PROCESS WILL WIPE YOUR DATA ON YOUR PHONE.

Useful links:
https://github.com/pawelik001/daisyinstall

In simple terms, go to Settings, enable Developer options, and check “Enable OEM unlock”. Then boot it into fastboot mode (by pressing power and volume -, until fastboot logo appears) plug your daisy_sprout to computer, and type the command into command line/powershell/terminal: fastboot oem unlock. This will unlock your bootloader and allow to flash custom ROM’s, modify your device etc.

2. Recoveries

Useful links:
Recoveries spreadsheet:
https://docs.google.com/spreadsheets/d/1zunbZBh_HoFj4iUsffqQFc3dmuBKzAGp3xku22kJqwg/edit?usp=sharing
https://github.com/pawelik001/daisyinstall

To install ROM, kernel or any other modifications, you need a recovery.
At the moment, we have 5 recoveries.
Official TWRP- generally little unstable, not recommended, sometimes error:1
Offain/@33bca TWRP- stable, encryption not working, perfect for daily use, sometimes error:1 too
OrangeFox- encryption not working, can't flash GSI, 
Deestroy- can’t flash ROM’s, unstable, not recommended
SHRP (SkyHawk Recovery Project)- ROM that you flash will not boot, not recommended
To start working with custom recovery, turn off your phone for 15 seconds, boot it into fastboot mode (by pressing power and volume -, until fastboot logo appears) plug your daisy_sprout to computer, and type the command into command line/powershell/terminal: fastboot boot <recoveryname>.img

NOTE: After flashing ROM, flash <recoveryinstaller>.zip, because after flashing ROM, you need to change slot, to slot, where recovery isn't installed, so flashing <recoveryinstaller>.zip every ROM flash/update is mandatory!!

3. Flashing ROM

Useful links:
ROMs spreadsheet: 
https://docs.google.com/spreadsheets/d/1I1XPH3LjLmlyDED3YJM0Sqp-wTIEqM3uKeUwWx8VPxs/edit?usp=drivesdk
https://github.com/pawelik001/daisyinstall

There you have a spreadsheet with all ROMs available for our device. From this spreadsheet you can read Android version, ROM version, maintainer, last update, if ROM is official or not, etc...
...and complete tutorial on how to flash a ROM on daisy_sprout. Originally, this is taken from tkchn https://github.com/tkchn/daisyinstall/ and modified, again, by me.
4. Kernels:

Useful links: https://docs.google.com/spreadsheets/d/1FnVxHI9TBeGP7tn_oRNdtSlWjMUcwwfVkbwyzO5AEj0/edit?usp=drivesdk

Generally, there are one active kernel developer:

-eremetein (eternityson)- who made Butterfly and Dragonheart kernels, overclocked, underclocked etc.

As everyone knows, our device is running on Snapdragon 625 (msm8953) with 8 cores at 2000MHz of frequency, and have Adreno 506 GPU with 650MHz of frequency by stock.

To explain:
According to Wikipedia...
"In computing, overclocking is the practice of increasing the clock rate of a computer to exceed that certified by the manufacturer. Commonly operating voltage is also increased to maintain a component's operational stability at accelerated speeds."

So basically overclocking is making frequency higher than it should be. 

But what is undervolting?
Again, according to Wikipedia…
"Undervolting is reducing the voltage of a component, usually the processor, reducing temperature and cooling requirements, and possibly allowing a fan to be omitted."

Is it possible to overclock CPU and undervolt it? Of course, it is.

Overclocked-
 -CPU- there are two variants, CPU can be overclocked to 2200MHz or 2400MHz,
 -GPU- there are two variants too, overclocked to 725MHz and 750MHz.

Underclocked-
 -There are only two versions, with undervolted CPU, and with undervolt + overclock.

5. Flashing GSI

GSI installation: https://docs.google.com/document/d/1F8nCU2Pt46SHjcCmgfiCQWuH547GDrY-hTOQjostVVA
And yes, that's all!

6. Guides

Better battery backup: https://telegra.ph/A-Guide-To-Achieve-Best-SOT-07-14
GSI installation: https://docs.google.com/document/d/1F8nCU2Pt46SHjcCmgfiCQWuH547GDrY-hTOQjostVVA
WiFi fix on custom roms with custom kernel.
https://docs.google.com/document/d/1ciyylNkNL26k3ITTFHVXBW9nrnv5ge3uOjIviyuAyq4
How to fix goodix fingerprint on gsi pie base: https://docs.google.com/document/d/1_glpDmgdcCap0wDtFupncairD7QQlaySyH3LZMTL6dI
Sound mod: https://docs.google.com/document/d/1bPW7m9aX2srwC38B3fkwvR5UDOmIcICYAySyaOpsiyQ
Unlock more LTE bands: https://drive.google.com/file/d/1M7ubCtX8bkJXFx79wbephc7-pvmnlW_6/view

7. Files

Some useful files folderon Google Drive, like camera2api enabler, stock repartition, splashes:
https://drive.google.com/drive/folders/1_YgHv-Cv6Ied465JLPwu9NXlMSURR1Ji

8. Other

Mi A2 Lite groups on telegram:
Mi A2 Lite Official: https://t.me/A2LiteOfficial
Mi A2 Lite Global: https://t.me/mia2lite_global
Mi A2 Lite MIUI: https://t.me/daisymiui
pawelik work: ("pre-release" information about SuperiorOS updates appears here) https://t.me/joinchat/JpyFhEgwQVWj9hfW7uwLzA
Mi A2 Lite photography: http://t.me/mia2litephotography
EvolutionX for daisy: http://t.me/EvolutionXDaisy

Language-specific groups:
Turkish: http://t.me/mia2liteturkiye
French: http://t.me/daisyfr
Brasil: http://t.me/miA2LitebR
Bangladesh: http://t.me/XiaomiA2LiteBD
Russian: http://t.me/mi_a2lite_ru
Poland: https://t.me/mia2litepoland



List of all contributors:
-pawelik001, for concept and for making this thread
-JanTabs, for help
-all developers of ROM's, kernels and all mods! 
Huge heart! <3

Also, you can contribute, by visiting this link: https://github.com/pawelik001/daisy_xda_megathread and doing pull request!
