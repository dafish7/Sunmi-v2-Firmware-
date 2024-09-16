
## "Un-Sunmi" and how to fix ADB

If you encounter "device unauthorized" after you disabled all sunmi apps on the device, this might help you.
I assume you got root, if not use the image or https://github.com/JunioJsv/mtk-easy-su
 
Starting point for this guide is a factory reset device.
Accept the terms and tap the "Experience" button when the device asks for a Wifi.

You'll be in "Experience Mode" with a countdown bubble - you get 30 minutes to do the following:

This is still a workaround until we find a way to get ADB working as intended. 

#### 1. Enable developer settings and enable USB-Debugging

Connect your device to your PC and do `adb shell` to test the connection. There should appear a toast "Debugging success".
Exit the shell afterwards.

#### 2. Install a terminal emulator and a file browser.

https://f-droid.org/de/packages/jackpal.androidterm/
https://f-droid.org/de/packages/com.martinmimigames.simplefileexplorer/

The Terminal is used to enable ADB because you will loose ADB after disabling all sunmi packages. 
The file explorer is needed as soon as you disable all sunmi packages or you wont be able to browse files without a explorer!

Doable via `adb install` or USB-Stick (if you plug one in there should be an notification about a drive - use "View" to browse the content)

#### 3. use `pm disable` or even better `pm uninstall --user 0` for all com.sunmi.* packages as well as woyou.market

Do this via `adb shell` on your PC or in the terminal app
 
#### 4. Use `pkill sunmi` to kill all running sunmi processes

The countdown bubble should disappear and you can relax, no more time pressure.

#### 5. Reboot the device

After reboot you should not have any sunmi trash left and you'll get the ADB error about being unauthorized. This is expected!

#### 6. Unplug your device from your PC
#### 7. open the terminal emulator and use `su` to switch to root, then `setprop ro.sunmi.welcome 1`
#### 8. Plug your device back into your PC and now ADB should work again.

  
This will keep ADB working until reboot. After reboot just repeat step 6 to 8.

## To have it "persistent" use Termux and Termux:boot

#### For this you need persistent root!

Download both from F-Droid (Imortant: Use only one source for termux and its add-ons! I suggest F-Droid)
Instructions for Termux:Boot can be found here: https://wiki.termux.com/wiki/Termux:Boot

Create a script with `su -c setprop ro.sundmi.welcome 1`