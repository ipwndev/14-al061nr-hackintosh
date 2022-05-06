# 14-al061nr-hackintosh
Skylake HP Pavilion Hackintosh EFI (OpenCore)

## Important ##

MacAddress and Serial Number are random, please re-set before use.  

## Hardware ##

| Hardware               | Model                                           | Support                       | Kext                                                       |
|------------------------|-------------------------------------------------|-------------------------------|------------------------------------------------------------|
| CPU                    | i3-6100u @2.3 GHz                               | Yes (Skylake)                 |                                                            |
| GPU                    | Intel HD 520 (Skylake GT2)                      | Yes (Without some DRM)        | WhateverGreen.kext                                         |
| Audio                  | Realtek ALC295                                  | Yes[1], Layout 13             | AppleALC.kext                                              |
| Ethernet               | RTL810xE PCI Express Fast Ethernet Controller   | Detected, not 100% functional | RealtekRTL8100.kext                                        |
| WiFi/ Bluetooth        | Intel Corporation Wireless 3165                 | Bluetooth and WiFi Supported  | AirportItlwm.kext                                          |
| SD Card Reader         | RTS522A PCI Express Card Reader                 | Yes (Read/Write)              | RealtekCardReader.kext and RealtekCardReaderFriend.kext    |
| Touchpad               | Intel Corporation Sunrise Point-LP-SMBUS(rev21) | Yes                           | VoodooRMI.kext, VoodooPS2Controller.kext, VoodooSMBus.kext |
| Battery                | Unknown HP 45Wh                                 | Yes                           | SMCBatteryManager.kext, ECEnabler.kext                     |
| Keyboard Function Keys |                                                 | Yes                           | BrightnessKeys.kext                                        |

## OpenCore Version ##

This config.plist was created for OpenCore 0.7.8 for MacOS BigSur

## Disclaimer ##
Use at your own risk, this is provided as a reference.

### Notes ###
[1] Audio at full volume is still quiet for output.  Microphone works at normal volume.  Using airpods or wired headphones results in adequate volume levels.  The speakers are what have reduced maximum volume.  