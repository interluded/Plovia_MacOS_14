What is Pluvia?
===============
Pluvia allows you to untethered downgrade your iPhone 4 without SHSH blobs! 
It uses the iOS 7.1.2 iBoot exploit "De Rebus Antiquis" by @xerub and @dora2-iOS.

Pluvia 1.6 Limitations
======================
Only for Mac!
Only supports iPhone3,1. 
- Support for iPhone3,2 and 3,3 is not easily possible because the iBoot exploit utilized by Pluvia has not been ported to those devices, and there is almost no documentation of how to do so.
Only supports iOS 5.1.1 (9B206), 6.x, and 7.x.
Can only jailbreak iOS 5.1.1 and 6.1.3

NOTE: 8GB iPhone 4's that shipped with iOS 6 can only run iOS 6 and newer, NOT iOS 4 or 5. This almost certainly can't be fixed.

How to use Pluvia
=================
1) Creating the patched IPSW

Run ./make_ipsw.sh <Input_IPSW> jailbreak (if you want to jailbreak)
Or run ./make_ipsw.sh <Input_IPSW> (if you don't want to jailbreak)

2) Restoring the firmware

Connect your iPhone 4 and put it in DFU mode.
Run ./restore.sh <Patched_IPSW>
Wait for that to complete.
When your phone reboots the Apple logo should blink and then it will boot the older iOS!

Getting out of recovery mode after restoring to stock iOS
=========================================================
Run ./make_ipsw.sh <Any_Supported_Input_IPSW> reset
Connect your iPhone 4 and put it in DFU mode.
Run ./restore.sh <Reset_NVRAM_IPSW>

Credits
=======
@xerub for De Rebus Antiquis iBoot exploit
@dora2-iOS for the auto-booting version of the exploit (ramdiskH_beta4.dmg), and the firmware bundles (https://github.com/dora2-iOS/s0meiyoshino)
@a8q for partitioning script in ramdisk
@saurik for Cydia.tar
UnthreadedJB for the iOS 5 untether
p0sixspwn (@ih8sn0w, @squiffy, @winocm) for the iOS 6 untether
s0uthwest, libimobiledevice, and @tihmstar for idevicerestore
@axi0mx for ipwndfu
@ih8sn0w, @NyanSatan, and @Merculous for iBoot32Patcher
@tihmstar and @encounter for tsschecker
@sequinn and @parrotgeek1 for root_tar

Licensing note
==============
The ParrotGeek Software logo shown during the restore process is NOT licensed under the GPL and must be removed in any forks.
Furthermore, any publicly released forks of this project must not use the word Pluvia anywhere in their name, or purport to be endorsed by ParrotGeek Software.
