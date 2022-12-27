# Sunmi-v2-Firmware-
my project on wiping and fully incorporating stock android on the leftover Deliveroo tablets in Australia, giving them a new lease on life   


So far i have managed to pull off the Firmware files, and sucessfully root it without compromising the verficiation intrgrigity. Unfortenly i have had to upload the files elsewhere because github doesnt like large files. Download from my website here: www.fishybytes.com

So heres the base firmware files, the firmware for presetup on the device, exactly right after hitting the factory restore option, right of the box expiernce. Flash it with SP flashtool using the mtk DA file in the folder 'Firmware', the scatter file in 'Firmware' and the auth file in root file of the rar. replace the boot file in the partition table (after loading the scatter file) with the magisk-patched file thats also in the root file of the rar. Use the 'Format all+Download' option, then hit downlaod and connect the cable to the turned off device. sit back and wait 5 minutes and it'll be ready. all you have to do after that is to set up the device, and install the latest magisk app. open the app, confirm the request to reboot to finish setting up magisk, and once rebooted its rooged and ready to customise the device. My next step is to flash stock android on there to remove the defalut sunmi stuff and fully incorperate the device for android. Due to the low specs od the device I wont be using any android version above 7.1.1, maybe 8 


Also the link for Discord server ive made for this Sunmi V2 to make helpiing other easier is https://discord.gg/9HRq7YPp
