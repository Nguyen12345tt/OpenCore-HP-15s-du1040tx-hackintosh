<h1 align="center"> macOS on HP 15s-du1040tx </h1>

<p align="center">
  <img src="https://github.com/Nguyen12345tt/OpenCore-HP-15s-du1040tx-hackintosh/blob/main/Resources/Screenshot%202025-01-02%20at%2016.07.51.png" alt="15s-du1040tx" width="750">
</p>

<h4 align="center"> OpenCore config for Hackintosh HP 15s-du1040tx </h4>

<p align="center">
<a href="https://www.apple.com/macos/sonoma-preview/">
  <img src="https://img.shields.io/badge/macOS-Ventura-yellow" width="170"/> </a>
<a href="https://github.com/acidanthera/OpenCorePkg/releases">
  <img src="https://img.shields.io/badge/OpenCore-1.0.3-9cf" width="160"/> </a>
<a href="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/releases">
  <img src="https://img.shields.io/badge/release-EFI-blue.svg" width="120"/> </a>
  <a href="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/issues"> 
  <img src="https://img.shields.io/badge/Changelog-orange.svg" width="108"/> </a>
</p>


## Table of Contents
  - [Screenshots](#screenshots-)
  - [Original Hardware](#original-hardware--)
  - [Modifications](#modifications--)
  - [macOS Update History](#macos-update-history)
  - [What's working](#whats-working--)
  - [Kexts Used](h#kext-used)
  - [SSDTs Used](#ssdt-used)
  - [Changelog](#changelog)
  - [Installation Steps](#installation-steps)
  - [How to make it better?](#how-to-make-it-better)
    - [Advanced Resolution](#advanced-resolution)
  - [Credits](#credits)
  - [Donate](#-donate---ba%C4%9F%C4%B1%C5%9F-)
  
## Screenshots 📷

### Sonoma
<p align="center">
  <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/macOS%20Desktop/Sonoma-14-3.png">
</p>

<details>
<summary>Sonoma</summary>
<p align="center">
  <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/macOS%20Desktop/Sonoma.png">
</p>
</details>  
  
<details>
<summary>Ventura</summary>
<p align="center">
  <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/macOS%20Desktop/Ventura.png">
</p>
</details>

<details>
<summary>Monterey</summary>
<p align="center">
  <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/macOS%20Desktop/Monterey.png">
</p>
</details>

<details>
<summary>Big Sur</summary>
<p align="center">
  <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/macOS%20Desktop/Big%20Sur.png">
</p>
</details>

## Original Hardware  💻
Type | Spec | Status
:---------|:---------|:----------
Model Name      | HP 15s-du1040tx | ✅
CPU              | Intel(R) Core(TM) i7-10510U CPU @ 1.80GHz Comet Lake | ✅
RAM           | 16GB 2667 MHz DDR4 | ✅
Internal Graphics Card | Intel(R) UHD Graphics (1536 MB) | ✅
Wi-Fi             | Realtek RTL8821CE | ❌
Ethernet          | Realtek RTL8111/8168/8411 | ✅
Audio       | Realtek ALC236 | ✅
Touchpad | I2C TouchPad | ✅

  
## Modifications  🔨
Type | Spec | Status
:---------|:---------|:----------
USB Wi-Fi | Tp-Link Archer T2U | ✅ 

- RTL8821CE not working on macOS. We have to use Intel Wi-Fi, USB Wi-Fi and Broadcom Wi-Fi.
- You have to install USB drivers for working USB adapter.

## macOS Update History
- ✅ macOS Sonoma 14.0 (Currently testing)
- ✅ macOS Ventura 13.6.7 (Currently using)
- ✅ macOS Monterey 12.6
- ✅ macOS Big Sur 11.7.3


## What's working  💻
Type | Status
:---------|:---------
Turbo boost and CPU frequency stage |  ✅
Intel UHD Graphics                  |  ✅
Brightness control                  |  ✅
HDMI                                |  ✅
Audio Realtek ALC236                |  ✅
Realtek Ethernet RTL8111            |  ✅
TP-Link Archer T2U Wi-Fi, Handoff, SideCar, iMessage..         |  ✅
USB 3.0 and Type-C (with Port Map)        |  ✅
Touchpad (14 gestures are working)   |  ✅
Battery status   |  ✅
Camera   |  ✅
S3 Sleep / Wake   |  ✅
S4 Hibernation / Wake   |  ✅
Shutdown / Reboot   |  ✅
Fn shortcut keys   |  ✅
  
## Kext Used
Kext | Info | MinKernel | MaxKernel
:---------|:---------|:---------|:---------
[Lilu](https://github.com/acidanthera/Lilu) | An open source kernel extension bringing a platform for arbitrary kext, library, and program patching throughout the system for macOS.
[VirtualSMC](https://github.com/acidanthera/VirtualSMC) | Advanced Apple SMC emulator in the kernel. Requires Lilu for full functioning.
[SMCBatteryManager](https://github.com/acidanthera/VirtualSMC) | a member of VirtualSMC that parses battery info.
[SMCProcessor](https://github.com/acidanthera/VirtualSMC) | a member of VirtualSMC that provides power info of processor temperature.
[WhateverGreen](https://github.com/acidanthera/WhateverGreen) | Various patches necessary for certain ATI/AMD/Intel/Nvidia GPUs. This is needed for Intel HD 620.  
[AppleALC.kext](https://github.com/acidanthera/AppleALC) | An open source kernel extension enabling native macOS HD audio for not officially supported codecs without any filesystem modifications. 
[NVMeFix](https://github.com/acidanthera/NVMeFix) | NVMeFix is a set of patches for the Apple NVMe storage driver, IONVMeFamily. | 18.0.0 |  22.9.9
[CPUFriend](https://github.com/acidanthera/CPUFriend) | A Lilu plug-in for dynamic power management data injection. | 10.0.0 |  
[CPUFriendDataProvider](https://github.com/corpnewt/CPUFriendFriend) | A CPUFriend plug-in for CPU power management. | 10.0.0 |  
[VoodooPS2Controller](https://github.com/acidanthera/VoodooPS2) | Contains updated Voodoo PS/2 Controller, improved Keyboard & Synaptics TouchPad. | 15.0.0 |  
[BrightnessKeys](https://github.com/acidanthera/BrightnessKeys) | Automatic handling of brightness keys based on ACPI Specification. | 16.0.0 |  
[RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X) | OS X open source driver for the Realtek RTL8111/8168 family. |  |  
[RtWlanU](https://github.com/chris1111/Wireless-USB-OC-Big-Sur-Adapter) | USB Wi-Fi adapter. |  |  
[RtWlanU1827](https://github.com/chris1111/Wireless-USB-OC-Big-Sur-Adapter) | USB Wi-Fi adapter. |  |  
[HoRNDIS9.2](https://github.com/jwise/HoRNDIS) | Android USB Tethering. |  |  
[UTBMap](https://github.com/USBToolBox/tool) | Kext to inject mapped USB ports |  |  
  
## SSDT Used
SSDT | Info | Status
:---------|:---------|:---------

[SSDT-EC-USBX](https://dortania.github.io/Getting-Started-With-ACPI/Universal/ec-fix.html#fixing-embedded-controller-ssdt-ecusbx) | Adds a fake Embedded Controller (SSDT-EC) and enables USB Power Management (SSDT-EC-USBX). | Functional
[SSDT-PLUG](https://dortania.github.io/Getting-Started-With-ACPI/Universal/plug.html#fixing-power-management-ssdt-plug) | Allow the kernel's XCPM(XNU's CPU Power Management) to manage CPU's power management. | Functional
[SSDT-PNLF](https://dortania.github.io/Getting-Started-With-ACPI/Laptops/backlight.html) | Adds Backlight Control for Laptop Screens. | Functional
[SSDT-SBUS-MCHC](https://dortania.github.io/Getting-Started-With-ACPI/Universal/smbus.html) | Fixes System Management Bus and Memory Controller in macOS. | Functional

## boot-args Used
boot-arg | Info
:---------|:---------
-v | Enables verbose.
debug=0x100 | This disables macOS's watchdog which helps prevents a reboot on a kernel panic.
keepsyms=1 | This is a companion setting to debug=0x100 that tells the OS to also print the symbols on a kernel panic.
alcid=xxx | Used for setting layout-id for AppleALC, see [supported codecs](https://github.com/acidanthera/applealc/wiki/supported-codecs) to figure out which layout to use for your specific system. More info on this is covered in the [Post-Install Page](https://dortania.github.io/OpenCore-Post-Install/) |

## Changelog

<details>
<summary>2024-12-30</summary>

- <b>Added</b>
  - Kernel
    - Add
      - USBPorts: For macOS Sonoma.
      - RtWlanU: USB Wi-Fi Adapter for macOS Sonoma.
      - RtWlanU1827: USB Wi-Fi Adapter for macOS Sonoma.
  - NVRAM
    - 7C436110-AB2A-4BBB-A880-FE41995C9F82
      - bluetoothExternalDongleFailed
        - 00 : Bluetooth Support for macOS 13.4 and later.
      - bluetoothInternalControllerInfo
        - 0000000000000000000000000000 : Bluetooth Support for macOS 13.4 and later.
      - boot-args
        - -lilubetaall for macOS Sonoma.
        - -no_compat_check for macOS Sonoma.
- <b>Changed</b>
  - Kernel
    - Add
      - NVMEFix: Max Kernel 22.9.9. Because macOS Sonoma not supported.
  - NVRAM
    - 7C436110-AB2A-4BBB-A880-FE41995C9F82
      - csr-active-config
        - 03080000 for USB Wi-Fi Adapter.
  - PlatformInfo
    - SMBIOS to MBP15,1 for macOS Sonoma installation. Change to 14,1 after installation.
- <b>Removed</b>
  - ACPI
    - Add
      - SSDT-KBD.aml: Useless
  - Kernel
    - Add
      - USBToolBox
      - UTBMap
  
</details>  

<details>
<summary>2023-04-25</summary>

- <b>Added</b>
  - Kernel
    - Add
      - USBToolBox: Inject Mapped USB ports.
      - UTBMap: USB port map.
- <b>Removed</b>
  - Kernel
    - Add
      - USBMap
      - USBMapLegacy
  
</details>  
  
<details>
<summary>2022-04-25 21:43</summary>

- <b>Added</b>
  - DeviceProperties
    - Ethernet
      - ´built-in 01 DATA´ for en0.
  - Kernel
    - Add
      - Min and Max Kernel Values
      - USBMap: Mapped USB ports for Catalina and newer.
      - USBMapLegacy: Mapped USB ports for Mojave and older.
      - BrcmBluetoothInjector: Bluetooth injection for Big Sur and older.
      - BrcmPatchRAM2: Bluetooth injection from Sierra to Mojave.
- <b>Changed</b>
    - Kernel
      - Quirks
        - CustomSMBIOSGuide: False
    - Misc
      - Boot
        - LauncherOption: Full
    - PlatformInfo
      - UpdateSMBIOSMode: Create
    - UEFI
      - Input
        - PointerSupport: False
- <b>Removed</b>
  - Kernel
    - Add
      - VoodooPS2Mouse
  
</details>
  
<details>
<summary>2022-03-25 16:25</summary>

- <b>Added</b>
  - Kexts
    - SMCBatteryManager: For true graphic in System Preferences.
    - RestrictEvents: For changed CPU name on About This Mac. (Intel(R) Core(TM) i5-7200U CPU @ 2.50GHz)
    - USBToolBox: Injects UTBMap.kext.
    - UTBMap: Mapped USB Ports.
- <b>Changed</b>  
    - config
      - Edited for CPU name. Don't change CPUType value.
        - Intel(R) Core(TM) i5-7200U CPU @ 2.50GHz. 
- <b>Removed</b>
  - Kexts
    - ACPIBatteryManager: Battery graphic issue on System Preferences.
    - SMCSuperIO: Laptop doesn't have a fan sensor.
    - USBInjectAll: No need anymore.
    - USBPorts: USBToolBox and UTBMap is using now.
  
</details>
  
<details>
<summary>2022-03-23 18:35</summary>

- <b>Added</b>
  - Kexts
    - BrightnessKeys: Brightness control on keyboard.
      - ACPI Patch
        - Rename (NBCF, 0x00) to Name (NBCF, 0x01)
- <b>Disabled</b>
  - ACPI
    - SSDT-CLICKPAD some compabilty problems.
    - SSDT-KBD
      - Using BrightnessKeys.kext and ACPI patch.
      - Disabled Rename _Q14 to XQ14 (TP-up)
      - Disabled Rename _Q15 to XQ15 (TP-down)
</details>

<details>
<summary>2022-03-23 15:15</summary>

- <b>Added</b>
  - ACPI
    - SSDT-AC for AC adapter in IORegistryExplorer.
    - SSDT-CLICKPAD for better touchpad.
    - SSDT-DMAC for DMAC device in IORegistryExplorer.
    - SSDT-EXT5-TP-LED for fix led on power button.
    - SSDT-FWHD for FWHD device in IORegistryExplorer.
    - SSDT-KBD for brightness control from keys.
      - ACPI Patch
        - Rename PNLF to XNLF
        - Rename _Q14 to XQ14 (TP-up)
        - Rename _Q15 to XQ15 (TP-down)
    - SSDT-PMC 
    - SSDT-PTSWAK for better sleep and wake.
      - ACPI Patch
        - Name0D-03 to 00
        - Name0D-04 to 00
        - Name6D-03 to 00
        - Name6D-04 to 00
        - Rename _PTS to ZPTS(1,N)
        - Rename _WAK to ZWAK(1,N)
    - SSDT-PWRB-SLPB_STA0B for power and sleep button.
    - SSDT-RTC_STA0F for enable RTC device.
  - Kexts
    - ACPIBatteryManager: For AppleSmartBatteryManager on IORegistryExplorer.
- <b>Changed</b>
  - ACPI
    - SSDT-XOSI to SSDT-OC-XOSI
      - ACPI Patch
        - Rename _OSI to XOSI (OS)
  - Kexts
    - FeatureUnlock 1.0.7 to 1.0.6 for fix Airplay to Mac.
- <b>Removed</b>
  - Kexts
    - SMCBatteryManager: Because using ACPIBatteryManager.kext
    - SMCLightSensor: Because laptop doesn't have a sensor.
  
</details> 

## Installation Steps

### Downloading OSX Image
- Click to OneDrive link and download it.
  - [Ventura](https://github.com/yusufklncc/Hackintosh-for-All-Computers#-macos-ventura-)
  - [Monterey](https://github.com/yusufklncc/Hackintosh-for-All-Computers#macos-monterey)
  - [Big Sur](https://github.com/yusufklncc/Hackintosh-for-All-Computers#macos-big-sur)
  - [Catalina](https://github.com/yusufklncc/Hackintosh-for-All-Computers#macos-catalina)
  
### Writing OSX Image
- Unzip the zip file to desktop.
- Download [balenaEtcher](https://www.balena.io/etcher/).
- Open program and click to `Flash from file`.
- Select the OSX image `.raw` file from the popup window.
- Click to `Select target` and select OSX image.
- Click to `Flash!` and allow app in popup window.
<p align="center">
  <img src="https://user-images.githubusercontent.com/78423442/154849816-0a04602a-9064-4780-9d4e-ed86254b4fea.png">

- When writing is finished, `remove` the USB stick and plug it back in.

### Setting EFI Folder
- When you plug USB back, you can see EFI partition in "My Computer"
- Open EFI partition.
- Delete default files.
- Copy downloaded EFI folder to EFI partititon.
- Open EFI/OC and set your config file. 
  - If you have Qualcomm Wi-Fi card. Delete default config and rename other one.
- Now you can boot from USB.

### Setting BIOS Settings 
  - Before you start, reset your BIOS settings to default.
  - `Disable`
    - Secure Boot
  - `Enable`
    - CSM
    
### macOS Installation
- Now let's turn off our computer and boot from USB. Choose the `Install macOS Monterey` (whatever you have) option on OpenCore menu and go to the installation screen.
- <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Installation/macOS%201.png">
- What to do on the following screens:
  - Select language and continue.
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Installation/macOS%202.png">
  - Open `Disk Utility` from the menu to prepare our disk.
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Installation/macOS%203.png">
  - Select `Show All Devices` from the `View` option and select the name of our disk and click `Erase`.
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Installation/macOS%204.png">
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Installation/macOS%205.png">
  - Rename the disk and erase as `APFS/GUID`.
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Installation/macOS%206.png">
  - Now close `Disk Utility` and select `Install macOS Sonoma` then next next next.
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Installation/macOS%208.png">
  - Select renamed disk and click continue.
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Installation/macOS%2010.png">
  - When the installation is finished,  `macOS Installer` option will be selected automatically every boot step until this option is `gone`.
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Installation/macOS%2011.png">
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Installation/macOS%2012.png">
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Installation/macOS%2013.png">
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Installation/macOS%2014.png">
  - After last boot, the language selection screen will welcome us. Select language and continue.
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Installation/macOS%2015.png">
  - Don't login `iCloud` account and continue. Because we need to set our `serial numbers and ROM for iCloud and iMessage`.
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Installation/macOS%2016.png">
  - Now we can see `Desktop`.
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Installation/macOS%2017.png">

### Post Installation

<br>

<details>
<summary><b>Broadcom Wi-Fi - Sonoma</b></summary>
  
- Dowload and Open [OCLP](https://github.com/dortania/OpenCore-Legacy-Patcher/releases). Click `Post-Install Root Patch` button.
<img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Broadcom%20Wi-Fi%20Activation%20-%20OCLP/oclp-menu.png">
- Click `Start Root Patching`.
<img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Broadcom%20Wi-Fi%20Activation%20-%20OCLP/post-install-menu.png">
- Click `Yes` and type password.
<img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Broadcom%20Wi-Fi%20Activation%20-%20OCLP/start-root-patch.png">
<img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Broadcom%20Wi-Fi%20Activation%20-%20OCLP/root-patching.png">
<img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Broadcom%20Wi-Fi%20Activation%20-%20OCLP/root-patching-2.png">
- Click `Reboot`
<img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Broadcom%20Wi-Fi%20Activation%20-%20OCLP/reboot-apply.png">
- Wi-Fi started working.
<img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/Broadcom%20Wi-Fi%20Activation%20-%20OCLP/sonoma-wifi.png">
  
</details>  

- Open config file with `Text Edit`.
  - Search `HideAuxiliary` and change `false` value to `true`.
  - Search `SecureBootModel` and change `Disabled` value to `Default`.
    - If you have patched your system with `OCLP`, do not do this step.
  - Search `boot-args` and delete `-v` argument.
- Now we have to set our serial numbers and ROM value.
  - Download [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS/archive/refs/heads/master.zip) and open .command file. If program asks `Download Python` download it. After that select option 3.
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/GenSMBIOS/GenSMBIOS%201.png">
  - Now list 5 SMBIOS first. `MacBookPro14,1`
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/GenSMBIOS/GenSMBIOS%202.png">
  - Select and copy first Serial.
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/GenSMBIOS/GenSMBIOS%203.png">
  - Go [check](https://checkcoverage.apple.com/) serial number. Your serial should be like this. If not, try second serial.
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/GenSMBIOS/Check%20Serial.png">
  - Search MacBookPro15,1 and replace `Type > SystemProductName, Serial > SystemSerialNumber, Board Serial > MLB and SmUUID > SystemUUID` values. Now we will set our ROM value.
  - Go `System Setting > Netwotk > Ethernet > Details > Hardware`. If our MAC adress is `54:1A:AF:43:70:CA` remove `:` characters = `541AAF4370CA`. Convert it to [Base64](https://base64.guru/converter/encode/hex). 
  - Now we have `VBqvQ3DK`. Replace this with ROM value and save config file.
  - Delete default `USBPorts` kext in OC/Kexts and rename other one to `USBPorts`.
  - Restart computer and press `Space` key on OpenCore menu. Then enter `ResetNVRAM`. After that BIOS settings may change. Check it and boot macOS.
  - Now you can login iCloud, iMessage or other apple services and you can use macOS.

## How to make it better?
<details>  
  <summary> <h3>Advanced Resolution</h3> </summary>

- Use RDM for 1600x900 resolution which i am using currently. 
  - [Download RDM](https://onedrive.live.com/download?cid=83E8AF2D3EA2BA57&resid=83E8AF2D3EA2BA57%214113&authkey=ALMpGB-on3pqMmY)
  
- 1366x768
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/RDM/1366x768.png" alt="1366x768" width="600"> 
- 1600x900 
  - <img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/RDM/1600x900.png" alt="1600x900" width="600">
 
## How to Use?
- Download and open RDM.app. Follow images below.
<img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/RDM/RDM%201680x1050.png" alt="1680x1050" width="600"> 

- Set resolution 1680x1050.
<img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/RDM/RDM%20Edit%20Button.png" alt="RDM Edit Button" width="600"> 

<img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/RDM/RDM%20Resolution%20Settings.png" alt="RDM Resolution Settings" width="600"> 

- Set what resolution you want. Click save, enter password and reboot.
<img src="https://github.com/yusufklncc/Lenovo-Thinkpad-E570-Hackintosh/blob/main/Resources/RDM/RDM%201600x900.png" alt="1600x900" width="600">  

- Open RMD and select resolution what you want. This is only once.
</details>  
      
## Credits
  
 - [Dortania](https://dortania.github.io) for developing OpenCore.
 - [Apple](https://www.apple.com) for macOS.
 - [Acidanthera](https://github.com/acidanthera) for most of the kexts.
 - [RehabMan](https://github.com/RehabMan) for battery patches.
 - [Sniki](https://github.com/Sniki) for USB kext.
 - And anyone else that helped to develop and improve hackintoshing.

<h1 align="center"> Donate - Bağış </h1>
<p align="center">
<a href="https://github.com/yusufklncc/yusfklncc/blob/main/Donate%20-%20Ba%C4%9F%C4%B1%C5%9F.md">
  <img src="https://github.com/yusufklncc/yusfklncc/blob/main/Resources/Donate.png" width="300">
