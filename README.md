# Acer-A515-54G-Hackintosh-OpenCore

#### Supports MacOS 11.6 & Updated to Monterey 12.0

<p align="center">
  <img src="https://raw.githubusercontent.com/adeelpm/Acer-Aspire-A515-54G-CPU-i5-8265u/main/Images/About_Mac.png" alt="Specs">
</p>

## Specs

|Model|Acer Aspire 5 A515-54G-55E4|
|---|---|
|CPU|8th Gen i5-8265U|
|GPU|intel UHD 620|
|SSD|512 GB NVME.m2|
|RAM|8GB|
|Ethernet|Realtek RTL|
|Wifi Adapter|Intel AC-9560|
|Bluetooth|Intel AC-9560|
|Keyboard|ps2 keyboard|
|Trackpad|I2C Elan 0504|

## Working Status

- [x] Dual boot Windows 11 + MacOS Monterey
- [x] Internal Audio and Headphone Jack
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

## Installation 

### BIOS Settings
* *Security* → Set supervisor password (to disable secure boot)
* *Security* → Password on boot → **Disable**
* *Boot* → Secure Boot → **Disable**
* *Boot* → Boot Mode → **UEFI**
* *Main* → Lid Open resume → **Enabled**
* *Advance settings* → CFG-Lock → **Disabled**

###  Basic Installation

- Create a Bootable USB for MacOS by using by Dortania's [OpenCore-Install-Guide](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/).
- Install MacOS to SSD / Hard drive. (While installing, connect USB keyboard and mouse).
- Copy **ALL** the Contains of this Repo inside the EFI partition of SSD / Hard drive.
- **[IMPORTANT]** Make sure to Generate system definitions of MacBook pro 15,4 in config.plist file using [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) & add `SystemSerialNumber`, `SystemUUID` and `MLB`.

### Post Installation
- If you have Installed MacOS on SSD, Enable TRIM using following command:

```sh

$ sudo trimforce enable

```


<p align="center">
<b>⭐ Please consider starring this repository if it helped you! ⭐</b>
</p>
