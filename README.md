# Acer-A515-54G-Hackintosh-OpenCore

#### Supports MacOS 11.4

<p align="center">
  <img src="https://i.imgur.com/q7VSJPa.png" alt="Specs">
</p>

## Specs

|Model|Acer Aspire 5 A515-54G-55E4|
|---|---|
|CPU|8th Gen i5-8265U|
|GPU|intel UHD 620|
|SSD|512 GB NVME.m2|
|RAM|8GB|
|Ethernet|Realtek RTL|
|Wifi Adapter|Intel|
|Bluetooth|Intel|
|Keyboard|ps2 keyboard|
|Trackpad|I2C Elan 0504|

## Working Status

- [x] Dual boot windows 10 + MacOS Bigsur
- [x] Internal Audio and Headphone Jack()
- [x] iGPU (have disabled discrete GPU)
- [x] Battery Management
- [x] Ethernet
- [x] Display Brightness and control with Keys
- [x] Sleep
- [x] Wifi + Bluetooth
- [x] USB2.0 ports
- [x] Webcam
- [x] Trackpad with multi finger gestures 
- [x] HDMI
- [x] Native hotkey support with Fn keys

 ### Known Issues
- Trackpad does not work with VoodooI2C kext but works with voodoops2(Place kext in correct order in config.plist)
- Battery life is just half of what I get in windows 

### Not Tested
- [x] Usb 3.0 + Type C

### Important
 Please add `SystemSerialNumber`, `SystemUUID` and `MLB`.

## Installation 

 ### BIOS Settings
* *Security* → Set supervisor password (to disable secure boot)
* *Security* → Password on boot → **Disable**
* *Boot* → Secure Boot → **Disable**
* *Boot* → Boot Mode → **UEFI**
* *Main* → Lid Open resume → **Enabled**

## Guide
1. This guide will help you from the start to the end : [Dortania Gitbook](https://dortania.github.io/OpenCore-Install-Guide/)
1. Generating Serial Number : 
GenSMBIOS from Corpnewt [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)

###  Basic Installation

- Create a Bootable USB for MacOS by using by Dortania's [OpenCore-Install-Guide](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/).
- Install MacOS to SSD / Hard drive. (While installing, connect USB keyboard and mouse).
- Copy **ALL** the Contains of this Repo inside the EFI partition of SSD / Hard drive.
- **[IMPORTANT]** Make sure to Generate system definitions of MacBook pro 15.2 in config.plist file using [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) & add `SystemSerialNumber`, `SystemUUID` and `MLB`.

### Post Installation
- If you have Installed MacOS on SSD, Enable TRIM using following command:

```sh

$ sudo trimforce enable

```


<p align="center">
<b>⭐ Please consider starring this repository if it helped you! ⭐</b>
</p>