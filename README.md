## Lollipop on your Nexus Android device

The easy way to install Android Lollipop.

You do not need to go through the complex process of installing the complete Android SDK.

You do not need Eclipse or Android installed.

## Files you need

Download this repo.

Download the correct factory image from https://developers.google.com/android/nexus/images

Decompress the files and copy the files along side the dab and fastboot files. 

Open the flash-all.sh file using a text editor.

Add ./ in front of every line that starts with fastboot.

Save the changes.

## Installing the files on your phone.

Go to Settings > About Phone, scroll to Build Number and tap it 7 times.

Go to Settings > Developer Options and select USB Debugging box.

Make sure Nexus 5 is powered on, then connect it to your Mac.

Open up Terminal.

Test if device is connected by `./adb devices`. if you see a series of characters then you are ok to proceed.

then run `./adb reboot bootloader`

then run `./fastboot oem unlock`

Use volume button and power button in Nexus 5 to select the option to unlock device.
After some process, Nexus 5 will return to fastboot screen mode.
Restart the phone. It will go back to initial setup screen.
Your phone is now unlocked.

Turn off the phone. Then turn it on in fastboot mode by pressing power button and volume down at the same time.

Type `./flash-all.sh` in Terminal.

If circles are spinning, you may need to reboot your phone (turn it off and on again).

It should now begin Lollipop.

