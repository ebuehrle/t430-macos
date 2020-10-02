# ThinkPad T430 EFI for macOS Catalina 10.15.7

This is a repo which includes files required to run macOS Catalina 10.15.7 on a ThinkPad T430 (2349U2B) with Intel HD 4000 graphics, 1600x900 or 1920x1080 (B140HAN01.3 with converter breakout) display and BCM94360HMB wifi card.

These are the versions of software included in this repository:

* Clover r5122
* [AirportBrcmFixup](https://github.com/acidanthera/airportbrcmfixup/releases) 2.0.9
* [AppleALC](https://github.com/acidanthera/AppleALC/releases) 1.5.2
* [CodecCommander](https://bitbucket.org/RehabMan/os-x-eapd-codec-commander/downloads/) 2.7.1
* [HibernationFixup](https://github.com/acidanthera/HibernationFixup/releases) 1.3.5
* [IntelMausiEthernet](https://github.com/Mieze/IntelMausiEthernet) 1.0.3
* [Lilu](https://github.com/acidanthera/Lilu/releases) 1.4.7
* [VirtualSMC](https://github.com/acidanthera/virtualsmc/releases) 1.1.6
* [VoodooPS2Controller](https://github.com/acidanthera/VoodooPS2/releases) 1.9.2
* [WhateverGreen](https://github.com/acidanthera/whatevergreen/releases) 1.4.2

## Important info

* The BIOS whitelist must be removed to use the BCM94360HMB wifi card (requires Windows, [IVprep](https://github.com/n4ru/IVprep) and [1vyrain](https://github.com/n4ru/1vyrain))

* Don't put any kexts in /S/L/E or /L/E, Clover will load them automatically. If you have some already, delete them and rebuild your cache before rebooting.

* If you have a model with the 1366x768 display, make sure to set `ig-platform-id` in `config.plist` to `0x01660003`.

* Generate your DSDT and SSDT using [ssdtPRGen](https://github.com/Piker-Alpha/ssdtPRGen.sh/releases) and apply patches in T430-Catalina-patches.txt with [MaciASL](https://github.com/acidanthera/MaciASL/releases) (note the additional manual changes at the bottom)

* Don't forget to generate your own SMBIOS values!
