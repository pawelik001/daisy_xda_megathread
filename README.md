[SIZE="4"]Welcome all XDA users! Since most devices have something like “mega thread” for specific device, and our beloved Mi A2 Lite (daisy_sprout) doesn't have, I've decided to make one, maybe for someone who doesn't use Telegram it will be useful.

[B][U][SIZE="5"][COLOR="Red"]WARNING: We (creators of this post and all modifications) are not responsible for what happens to your phone! But remember, we can always do our best to help you! Happy modifications![/COLOR][/SIZE][/U][/B]

All guides are imported/modified/created/deleted from Telegram. 
So let's start!



CHAPTERS:
[HIDE]
[LIST=1]
[*]Prerequisites
[*]Unlocking bootloader
[*]Installing recoveries
[*]Flashing ROM’s
[*]Flashing kernels
[*]Flashing GSI
[*]Guides
[*]Files
[*]Others
[/LIST]
[/HIDE]

[B]0. Prerequisites[/B]

[HIDE][INDENT][SIZE="3"]There you have some useful files at start
*Minimal ADB and fastboot: [url]http://forum.xda-developers.com/showthread.php?t=2317790[/url]
*MiFlash for flashing stock rom: [url]https://xiaomifirmware.com/downloads/download-latest-version-mi-flash-tool-v-7-4-25/[/url]
*Nice tutorial containing almost everything written by tkchn, modified by me: [url]https://github.com/pawelik001/daisyinstall[/url]
*Brain, of course, to not ended up destroying your daisy_sprout, and to understand this thread

And useful spreadsheets, I will put here all of them, but in every chapter they will be too.
ROM’s: [url]https://docs.google.com/spreadsheets/d/1Uy6qouIV0WbVouK4X5PhmUz2quxfLguHDqSf6LYDBO8[/url]
Kernels: [url]https://docs.google.com/spreadsheets/d/1FnVxHI9TBeGP7tn_oRNdtSlWjMUcwwfVkbwyzO5AEj0[/url]
Recoveries: [url]https://docs.google.com/spreadsheets/d/1zunbZBh_HoFj4iUsffqQFc3dmuBKzAGp3xku22kJqwg[/url]
Files: [url]https://docs.google.com/spreadsheets/d/1I1XPH3LjLmlyDED3YJM0Sqp-wTIEqM3uKeUwWx8VPxs[/url][/SIZE][/INDENT][/HIDE]

[B]1. Unlocking bootloader[/B]

[HIDE][INDENT][SIZE="5"][B][U][COLOR="Red"]WARNING: 
THIS WILL VOID YOUR WARRANTY
BE SURE TO BACK UP YOUR INTERNAL STORAGE, AS THIS PROCESS WILL WIPE YOUR DATA ON YOUR PHONE.[/COLOR][/U][/B][/SIZE]

[SIZE="3"]Useful links:
*[url]https://github.com/pawelik001/daisyinstall[/url]

In simple terms, go to Settings, enable Developer options, and check “Enable OEM unlock”. Then boot it into fastboot mode (by pressing power and volume -, until fastboot logo appears) plug your daisy_sprout to computer, and type the command into command line/powershell/terminal: [CODE]fastboot oem unlock[/CODE]. This will unlock your bootloader and allow to flash custom ROM’s, modify your device etc.[/SIZE][/INDENT][/HIDE]

[B]2. Recoveries[/B]

[HIDE][SIZE="3"][INDENT]Useful links:
Recoveries spreadsheet:
*[url]https://docs.google.com/spreadsheets/d/1zunbZBh_HoFj4iUsffqQFc3dmuBKzAGp3xku22kJqwg/edit?usp=sharing[/url]
*[url]https://github.com/pawelik001/daisyinstall[/url]

To install ROM, kernel or any other modifications, you need a recovery.
At the moment, we have 5 recoveries.
[HIDE][LIST][*]Official TWRP- generally little unstable, not recommended, sometimes error:1
[*]Offain/@33bca TWRP- stable, encryption not working, perfect for daily use, sometimes error:1 too
[*]OrangeFox- encryption not working, can't flash GSI, 
[*]Deestroy- can’t flash ROM’s, unstable, not recommended
[*]SHRP (SkyHawk Recovery Project)- ROM that you flash will not boot, not recommended[/LIST][/HIDE]
To start working with custom recovery, turn off your phone for 15 seconds, boot it into fastboot mode (by pressing power and volume -, until fastboot logo appears) plug your daisy_sprout to computer, and type the command into command line/powershell/terminal: [CODE]fastboot boot <recoveryname>.img[/CODE]

[B][U]NOTE: After flashing ROM, flash <recoveryinstaller>.zip, because after flashing ROM, you need to change slot, to slot, where recovery isn't installed, so flashing <recoveryinstaller>.zip every ROM flash/update is mandatory!![/U][/B][/INDENT][/SIZE][/HIDE]

[B]3. Flashing ROM[/B]

[HIDE][SIZE="3"][INDENT]Useful links:
ROMs spreadsheet: 
[url]https://docs.google.com/spreadsheets/d/1I1XPH3LjLmlyDED3YJM0Sqp-wTIEqM3uKeUwWx8VPxs/edit?usp=drivesdk[/url]
[url]https://github.com/pawelik001/daisyinstall[/url]

There you have a spreadsheet with all ROMs available for our device. From this spreadsheet you can read Android version, ROM version, maintainer, last update, if ROM is official or not, etc...
...and complete tutorial on how to flash a ROM on daisy_sprout. Originally, this is taken from tkchn [url]https://github.com/tkchn/daisyinstall/[/url] and modified, again, by me.[/INDENT][/SIZE][/HIDE]

[B]4. Kernels:[/B]

[HIDE][SIZE="3"][INDENT]Useful links: [url]https://docs.google.com/spreadsheets/d/1FnVxHI9TBeGP7tn_oRNdtSlWjMUcwwfVkbwyzO5AEj0/edit?usp=drivesdk[/url]

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
 -There are only two versions, with undervolted CPU, and with undervolt + overclock.[/INDENT][/SIZE][/HIDE]

[B]5. Flashing GSI[/B]

[HIDE][INDENT][SIZE="3"]*GSI installation: [url]https://docs.google.com/document/d/1F8nCU2Pt46SHjcCmgfiCQWuH547GDrY-hTOQjostVVA[/url]
And yes, that's all![/SIZE][/INDENT][/HIDE]

[B]6. Guides[/B]

[HIDE][INDENT][SIZE="3"]Better battery backup: [url]https://telegra.ph/A-Guide-To-Achieve-Best-SOT-07-14[/url]
GSI installation: [url]https://docs.google.com/document/d/1F8nCU2Pt46SHjcCmgfiCQWuH547GDrY-hTOQjostVVA[/url]
WiFi fix on custom roms with custom kernel:
[url]https://docs.google.com/document/d/1ciyylNkNL26k3ITTFHVXBW9nrnv5ge3uOjIviyuAyq4[/url]
How to fix goodix fingerprint on gsi pie base: [url]https://docs.google.com/document/d/1_glpDmgdcCap0wDtFupncairD7QQlaySyH3LZMTL6dI[/url]
Sound mod: [url]https://docs.google.com/document/d/1bPW7m9aX2srwC38B3fkwvR5UDOmIcICYAySyaOpsiyQ[/url]
Unlock more LTE bands: [url]https://drive.google.com/file/d/1M7ubCtX8bkJXFx79wbephc7-pvmnlW_6/view[/url][/SIZE][/INDENT][/HIDE]

[B]7. Files[/B]

[HIDE][SIZE="3"][INDENT]Some useful files folderon Google Drive, like camera2api enabler, stock repartition, splashes:
[url]https://drive.google.com/drive/folders/1_YgHv-Cv6Ied465JLPwu9NXlMSURR1Ji[/url][/INDENT][/SIZE][/HIDE]

8. Other

[HIDE][INDENT][SIZE="3"]Mi A2 Lite groups on telegram:
[HIDE][LIST]
[*]Mi A2 Lite Official: https://t.me/A2LiteOfficial
[*]Mi A2 Lite Global: https://t.me/mia2lite_global
[*]Mi A2 Lite MIUI: https://t.me/daisymiui
[*]pawelik work: ("pre-release" information about SuperiorOS updates appears here) https://t.me/joinchat/JpyFhEgwQVWj9hfW7uwLzA
[*]Mi A2 Lite photography: http://t.me/mia2litephotography
[*]EvolutionX for daisy: http://t.me/EvolutionXDaisy
[/LIST][/HIDE]
Language-specific groups:
[HIDE][LIST]
[*]Turkish: http://t.me/mia2liteturkiye
[*]French: http://t.me/daisyfr
[*]Brasil: http://t.me/miA2LitebR
[*]Bangladesh: http://t.me/XiaomiA2LiteBD
[*]Russian: http://t.me/mi_a2lite_ru
[*]Poland: https://t.me/mia2litepoland
[/LIST][/HIDE][/SIZE][/INDENT][/HIDE]


List of all contributors:
-pawelik001, for concept and for making this thread
-JanTabs, for help
-all developers of ROM's, kernels and all mods! 
Huge heart! <3[/SIZE]

Also, you can contribute, by visiting this link: https://github.com/pawelik001/daisy_xda_megathread and doing pull request!
