# Infinix-Device-Gsi-install
Download Treble Info App 
And Check ✅ Your Device Type .
PLEASE READ RELATED SECTION IN README CAREFULLY AND THROUGHLY.

	##DISCLAIMER##
	-------
	I am not responsible for any problem you face.
	I made this script to flash Gsi on my device and its working great for me. 
	Use this script at your OWN RISK!


# If Your Device Support Project Treble You Can Continue...

• <a href ="/src/Treble_Info_5.2.3.apk" > Treble Info</a> 
<br>
•
<br>
•

<h1>Infinix Zero 5G X6815</h1>
<b>Testing Device</b> :Infinix Zero 5G (X6815)




<br>
<img src="https://github.com/Bikasmahanta/Infinix-Device-Gsi-install-And-Fix-/raw/refs/heads/main/trebleinfoX6815.jpg" width="360" alt="Treble info X6815" />







0.	After Unlocking BL developer options are turned off.
1.	Re-Enable Developer Options by tapping 7 times on "Build Number" in About section of your device.
2.	Navigate to Dev-Options and enable "USB Debugging" and make sure "OEM Unlock" is enabled/greyed out.
3.	Connect your phone with PC.
4.	Rename your downloaded xxx-Gsi.img to gsi.img and paste it in main folder
5.	Not every gsi is bug free - Root is required to fix some of them.
-------ho	READ CAREFULLY 	AND DO NOT PRESS KEY UNTILL PROGRAM ASK YOU TO PRESS.

Reboot phone to Fastboot mode 
bootloader mode

Wait till you see fastboot screen on your phone


	adb reboot bootloader

To reboot device to fastboot-D mode

	fastboot reboot fastboot

Rebooting into fastboot                            OKAY [  0.007s]

< waiting for any device >
Finished. Total time: 23.184s

first Erase System And TRy it gsi to flash Is it showing Error Somthing LIke This 

	fastboot erase system

C:\platform-tools>fastboot erase system

Erasing 'system_a'                                 
OKAY [  0.050s]
Finished. Total time: 0.085s



To delete logical/product partition - Required to create space for GSI

	fastboot delete-logical-partition product_a

Deleted logical partition sucessfully

	fastboot delete-logical-partition system_ext_a
 
• Deleted logical partition sucessfully


	fastboot flash system gsi.img

C:\platform-tools>fastboot flash system gsi.img


Resizing 'system_a'                                OKAY [  0.009s]

Sending sparse 'system_a' 1/9 (262116 KB)          OKAY [  8.958s]

Writing 'system_a'                                 OKAY [  0.677s]

Sending sparse 'system_a' 2/9 (262116 KB)          OKAY [  8.821s]

Writing 'system_a'                                 OKAY [  0.594s]

Sending sparse 'system_a' 3/9 (262100 KB)          OKAY [  8.793s]

Writing 'system_a'                                 OKAY [  0.604s]

Sending sparse 'system_a' 4/9 (262124 KB)          OKAY [  8.538s]

Writing 'system_a'                                 OKAY [  0.603s]

Sending sparse 'system_a' 5/9 (262124 KB)          OKAY [  8.632s]

Writing 'system_a'                                 OKAY [  0.606s]

Sending sparse 'system_a' 6/9 (262124 KB)          OKAY [  8.730s]

Writing 'system_a'                                 OKAY [  0.612s]

Sending sparse 'system_a' 7/9 (262124 KB)          OKAY [  8.691s]

Writing 'system_a'                                 OKAY [  0.621s]

Sending sparse 'system_a' 8/9 (262124 KB)          OKAY [  8.646s]

Writing 'system_a'                                 OKAY [  0.650s]

Sending sparse 'system_a' 9/9 (205284 KB)          OKAY [  6.798s]

Writing 'system_a'                                 OKAY [  0.652s]
Finished. Total time: 87.538s




Please wait till verification is disabled on both slots.

	fastboot --disable-verity --disable-verification flash vbmeta vbmeta.img

 C:\platform-tools>fastboot flash vbmeta_a vbmeta.img

Sending 'vbmeta_a' (4 KB)                          OKAY [  0.031s]

Writing 'vbmeta_a'                                 OKAY [  0.009s]
Finished. Total time: 0.091s



	fastboot reboot recovery

C:\platform-tools>fastboot reboot

Rebooting                                          
OKAY [  0.000s]
Finished. Total time: 0.016s






Once in recovery select Wipe and Factory Reset
-------
<br>
• First boot can take upto 5min. Wait till you see welcome screen
<br>


#NOT EVERY GSI IS BUG FREE - Root is required to fix some of the










# Tested GSi : Evelution X Gsi Android 14 (Unofficial)

Issues : Network problem In Starting No internet
Fix Internet Issue : 

"adb shell settings put global restricted_networking_mode 0"

Bug 🪲 : Incoming Call Not Showing Call,Anathor Mobile is  Ringing But Not Any Pop-Up In My Device
Didn't Try Any Other Call Ui App Its , Vendor Problem Or Something.




<h4>How to Fix WiFi/Internet/Network not working in GSI ROM</h4>

STEP 1: Install Android SDK

You have to install the Android SDK Platform Tools on your PC. This is the official ADB and Fastboot binary provided by Google and is the only recommended one. So download it and then extract it to any convenient location on your PC. Doing so will give you the platform-tools folder, which will be used throughout this guide.


STEP 2: Enable USB Debugging

Next up, you will have to enable USB Debugging so that your device is recognizable by the PC in ADB mode. This will then allow you to execute the desired ADB Commands. So head over to Settings > About Phone > Tap on Build Number 7 times > Go back to Settings > System > Advanced > Developer Options > Enable USB Debugging.

STEP 3: Execute ADB Shell Command

1.Connect your device to the PC via a USB cable. Make sure USB Debugging is enabled.

2.Then head over to the platform-tools folder, type in CMD in the address bar, and hit Enter.

3.This will launch the Command Prompt. So type in the below commands in the CMD window:



	adb shell settings put global restricted_networking_mode 0


STEP 4: If Step 3 Didn’t Work
If the aforementioned command didn’t work out, then root your GSI ROM via Magisk and proceed with the below steps:

1.Download and install the Termux app from F-Droid.
2.Then launch it and execute the following commands

	adb shell settings put global restricted_networking_mode 0


	su -c settings put global restricted_networking_mode 0

	su settings put global restricted_networking_mode 0



3.The underlying network issue should now be fixed.


That’s it. This should fix the WiFi/Internet/Network not working issue in GSI ROM. If you have any queries concerning the aforementioned steps, do let us know in the comments. We will get back to you with a solution at the earliest.

<br>

How to Fix Calling Issues in GSI ROM

1.Head over to Settings > Phh Treble Settings > IMS Features > Install IMS APK for Qualcomm Vendor.
2.The APK will now be downloaded. Once done, open it and enable Unknown Sources for the MTP Host.
3.The app will now be installed. Once done, enable “Request IMS Network” and “Force the presence of 4G Calling Setting”
4.Next up, open Dialer > Type *#*#4636#*#* > This will open the Testing Menu.
5.Go to the Phone Information > Select NR/LTE under Preferred Network Type.
6.Finally, restart the device and the calling feature will now work well and good.

Gsi Enable / Disable Command
 
Finally, type in the below command to make your device reboot to GSI every time.
adb shell gsi_tool enable
How to Undo this Change
If you want to revert the DSU Sideloader to its earlier working state i.e. switching between stock/custom and GSI ROM after every reboot, then carry out STEPS 1 to 4 listed above and execute the below command:

adb shell gsi_tool disable


Fix Fast Charging not working in GSI ROM
magisk module flash

https://drive.google.com/file/d/1KguCeLD-VHShm0MYzKhYrsAv-rZAuJeA/view




How to Fix Brightness Slider not working in GSI ROM

1.To begin with, head over to the Settings menu on your device.
2.Then go to Misc Features and checkmark Force alternative backlight scale.
3.Finally, reboot your device and the issue should be rectified



headphone jack fix gsi


adb shell
su 

setprop persist.sys.overlay.devinputjack true


active partition check fastboot 
fastboot getvar all


resize Product Partition
After that, type in the below command to set the size of the product partition to 0

fastboot resize-logical-partition product_a 0x0

(bootloader) partition-size:product_a:0x0

fastboot delete-logical-partition vendor

Then recreate it using the below command:

fastboot create-logical-partition vendor 0