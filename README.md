# 14-al061nr-hackintosh
Skylake HP Pavilion Hackintosh EFI (OpenCore)
MacAddress and Serial Number are random, please re-set before use.  This EFI mostly works, and I have been using this machine daily for about a month.  

## Hardware ##

| Hardware               | Model                                           | Support                          | Kext                                                       |
|------------------------|-------------------------------------------------|----------------------------------|------------------------------------------------------------|
| CPU                    | i3-6100u @2.3 GHz                               | Yes (Skylake)                    |                                                            |
| GPU                    | Intel HD 520 (Skylake GT2)                      | Yes (Without some DRM)           | WhateverGreen.kext                                         |
| Audio                  | Realtek ALC295                                  | Yes[1], Layout 13                | AppleALC.kext                                              |
| Ethernet               | RTL810xE PCI Express Fast Ethernet Controller   | Detected[2], not 100% functional | RealtekRTL8100.kext                                        |
| WiFi/ Bluetooth        | Intel Corporation Wireless 3165                 | Bluetooth and WiFi Supported[4]  | AirportItlwm.kext                                          |
| SD Card Reader         | RTS522A PCI Express Card Reader                 | Yes (Read/Write)                 | RealtekCardReader.kext and RealtekCardReaderFriend.kext    |
| Touchpad               | Intel Corporation Sunrise Point-LP-SMBUS(rev21) | Yes                              | VoodooRMI.kext, VoodooPS2Controller.kext, VoodooSMBus.kext |
| Battery                | Unknown HP 45Wh                                 | Yes[3]                           | SMCBatteryManager.kext, ECEnabler.kext                     |
| Keyboard Function Keys |                                                 | Yes                              | BrightnessKeys.kext                                        |
| Webcam                 | HP Camera over USB                              | Yes                              |                                                            |


## OpenCore Version ##

This config.plist was created for OpenCore 0.7.8 for MacOS BigSur.  I replaced the 512g, 5400RPM drive with a 240g PNY SSD. 8GB in single channel memory results in a useable machine.  

## Disclaimer ##
Use at your own risk, this is provided as a reference.

### Notes and Issues ###
[1] Audio at full volume is still quiet for output(roughly 50% of manjaro while at 100%).  Microphone works at normal volume.  Using airpods or wired headphones results in adequate volume levels.  The speakers are what have reduced maximum volume.  

[2] Ethernet Driver detects the card, and when a cable is connected.  Cant determine IP address or pass data in BigSur, this may be result of an outdated driver. 

[3] Battery Life is about 1.3 hours.  I recieved the laptop in a poor state. It was roughly 2 hours in Manjaro for comparision.  I believe the laptop wakes periodically, even when the lid is closed resulting in slightly worse battery life.  Pstates have been configured.  The machine only charges to ~74%.  Occasionally doesn't charge, battery indicator does not always reflect accurately.  These issues existed in Manjaro/Arch as well.    

[4] WiFi is occasionally slow(less than 30mbps on a 150mbps connection), and bluetooth does not have an independent toggle for power.  
