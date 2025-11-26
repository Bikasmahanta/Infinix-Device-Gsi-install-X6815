# Infinix-Device-Gsi-install
Download Treble Info App 
And Check ✅ Your Device Type .
PLEASE READ RELATED SECTION IN README CAREFULLY AND THROUGHLY.

	##DISCLAIMER##
	-------
	I am not responsible for any problem you face.
	I made this script to flash Gsi on my device and its working great for me. 
	Use this script at your OWN RISK!


 If Your Device Support Project Treble You Can Continue...

• <a href ="/src/Treble_Info_5.2.3.apk" > Treble Info</a> 
<br>
•
<br>
•

<h1>Infinix Zero 5G X 6815</h1>
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


To delete logical/product partition - Required to create space for GSI

	-------
fastboot delete-logical-partition product_a
Deleted logical partition sucessfully


fastboot delete-logical-partition system_ext_a
 

• Deleted logical partition sucessfully
fastboot erase system
 •    Deleted logical partition sucessfully





Please wait till verification is disabled on both slots.
fastboot --disable-verity --disable-verification flash vbmeta vbmeta.img

 • Verification disabled Sucessfully



fastboot reboot recovery






Once in recovery select Wipe and Factory Reset
-------
<br>
• First boot can take upto 5min. Wait till you see welcome screen
<br>


NOT EVERY GSI IS BUG FREE - Root is required to fix some of the




