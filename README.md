# Sunmi-v2-Firmware-
my project on wiping and fully incorporating stock android on the leftover Deliveroo tablets in Australia, giving them a new lease on life   


So far i have managed to pull off the Firmware files, and sucessfully root it without compromising the verficiation intrgrigity. Unfortenly i have had to upload the files elsewhere because github doesnt like large files. Download from my website here: www.fishybytes.com

So heres the base firmware files, the firmware for presetup on the device, exactly right after hitting the factory restore option, right of the box expiernce. Flash it with SP flashtool using the mtk DA file in the folder 'Firmware', the scatter file in 'Firmware' and the auth file in root file of the rar. replace the boot file in the partition table (after loading the scatter file) with the magisk-patched file thats also in the root file of the rar. Use the 'Format all+Download' option, then hit downlaod and connect the cable to the turned off device. sit back and wait 5 minutes and it'll be ready. all you have to do after that is to set up the device, and install the latest magisk app. open the app, confirm the request to reboot to finish setting up magisk, and once rebooted its rooged and ready to customise the device. My next step is to flash stock android on there to remove the defalut sunmi stuff and fully incorperate the device for android. Due to the low specs od the device I wont be using any android version above 7.1.1, maybe 8 


Also the link for Discord server ive made for this Sunmi V2 to make helpiing other easier is https://discord.gg/9HRq7YPp

Introducing Sunmi V2 TWRP!
Yes, I now have made a working TWRP recovery image, easy to install, but does **require root** first so take note of that.
Installation as goes:
Open cmd/terminal in directory where the recovery img is
type " adb push Sunmi_V2-TWRP.img /storage/emulated/0/Download" obviously without the quotation marks
once it finishes the command, type "adb shell"
followed by "su"
at this point your device should already have Magisk app installed, and is rooted, so you should have a small notification pop up asking if want to give shell Super User privileges accept, and the terminal should now have a "#" infront of the blinking cursor line, indicating that you are now SU in shell
type (VERY IMPORTANT DO NOT MISSTYPE AND MSKE SURE YOU HAVE FOLLOWED THE ABOVE STEPS TO THE LETTER) "dd =if/storage/emulated/0/Download/Sunmi_v2-TWRP.img of=/dev/block/platform/bootdevice/by-name/recovery" (again without the quotation marks)

If the command doesnt fail, than hooray! You now have twrp installed in your system recovery. now reboot to recovery (any method you want). Once the Orange boot splash screen turns off, after the printer makes a ose, the screen WILL GO BLACK, but dont worry, just press/tap the power button a few times and the display should turn back on in TWRP

BUT WAIT THERES MORE! unfourently, im not exactly 100% a genius, kinda accidently made the default language for TWRP Something other than english, but theres a fix to that: once you open twrp for the first time, you should be faced with two buttons above a sliding bar at the bottom of the screen, with a massive text of message on the top half. swipe the bar ( It WILL enable the partition to be mounted as read and write, so be careful, you can accidemtly do some damage if you dont know what your doing. If you feel more comfortable with the system being mounted ad read only, touch the left button instead of sliding the  bar.) you should now be faced with 8 buttons, the button on the seconf bottom right, is the options button. hit that. There should be a row of icon near the top of the screen, indication seperate pages for the option setion; touch the last oe, the one that looks like a globe. and scroll and select your desired language, and hit the button at the bottom of the screen, saving your selection