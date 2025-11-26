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

Rebooting into fastboot                            OKAY [  0.007s]
< waiting for any device >
Finished. Total time: 23.184s

first Erase System And TRy it gsi to flash Is it showing Error Somthing LIke This 

	fastboot erase system

#Log
C:\platform-tools>fastboot erase system
Erasing 'system_a'                                 OKAY [  0.050s]
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
Rebooting                                          OKAY [  0.000s]
Finished. Total time: 0.016s






Once in recovery select Wipe and Factory Reset
-------
<br>
• First boot can take upto 5min. Wait till you see welcome screen
<br>


NOT EVERY GSI IS BUG FREE - Root is required to fix some of the




