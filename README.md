Important Notice
================
This is a fork of plovia with an edited restore.sh to ensure compatibility with newer macOS versions.

Download Python2.7.18 from https://www.python.org/downloads/release/python-2718/
Then run restore.sh like normal,

Tested with 5.11 internalUI on a 16 GB iPhone 4.

No support will be given.

What is Plovia?
===============
plovia allows you to untethered downgrade your iPhone 4 without SHSH blobs!

It uses the iOS 7.1.2 iBoot exploit "De Rebus Antiquis" by @xerub and @dora2-iOS.

Limitations
===========
* Only for Mac!
* Only supports iPhone3,1.
  - Support for iPhone3,2 and 3,3 is not easily possible because the iBoot exploit utilized by plovia has not been ported to those devices, and there is almost no documentation of how to do so.
* Only supports iOS 5.1.1 (9B206), 6.x, and 7.x.
* Can only jailbreak iOS 5.1.1 and 6.1.3

**NOTE: 8GB iPhone 4's that shipped with iOS 6 can only run iOS 6 and newer, NOT iOS 4 or 5. This almost certainly can't be fixed.**

How to use plovia
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

@dora2-iOS for ramdiskH.dmg, part of the partitioning script in the ramdisk, the binaries in the ramdisk (which are likely from Cydia packages), and the firmware bundles

@a8q for the original partitioning script in the ramdisk

@saurik for Cydia.tar

UnthreadedJB for the iOS 5 untether

p0sixspwn (@ih8sn0w, @squiffy, @winocm) for the iOS 6 untether

s0uthwest, libimobiledevice, and @tihmstar for idevicerestore, which I patched in a hex editor to remove several error messages and skip checks that would make the restore fail

@axi0mx for ipwndfu

@ih8sn0w, @NyanSatan, and @Merculous for iBoot32Patcher

@tihmstar and @encounter for tsschecker

@sequinn and @parrotgeek1 for root_tar

@danzatt for ios-dualboot (hfs_resize)

https://github.com/mkropat/sh-realpath for realpath code used in scripts

libusb and pyusb
