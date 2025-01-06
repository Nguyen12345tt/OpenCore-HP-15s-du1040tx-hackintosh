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
<a href="https://github.com/Nguyen12345tt/OpenCore-HP-15s-du1040tx-hackintosh/releases">
  <img src="https://img.shields.io/badge/release-EFI-blue.svg" width="120"/> </a>
  <a href="https://github.com/Nguyen12345tt/OpenCore-HP-15s-du1040tx-hackintosh/issues"> 
  <img src="https://img.shields.io/badge/Changelog-orange.svg" width="108"/> </a>
</p>


## Table of Contents
  - [Original Hardware](#original-hardware--)
  - [Modifications](#modifications--)
  - [What's working](#whats-working--)
  - [Kexts Used](h#kext-used)
  - [SSDTs Used](#ssdt-used)
  - [Changelog](#changelog)
  - [Installation Steps](#installation-steps)

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
[Lilu](https://github.com/acidanthera/Lilu) | A kext to patch many processes, required for AppleALC, WhateverGreen, VirtualSMC and many other kexts. Without Lilu, they will not work.|
[VirtualSMC](https://github.com/acidanthera/VirtualSMC) | Emulates the SMC chip found on real macs, without this macOS will not boot.|
[SMCBatteryManager](https://github.com/acidanthera/VirtualSMC) | a member of VirtualSMC that parses used for measuring battery readouts on laptops.|
[SMCProcessor](https://github.com/acidanthera/VirtualSMC) | a member of VirtualSMC that provides used for monitoring Intel CPU temperature.|
[SMCSuperIO](https://github.com/acidanthera/VirtualSMC) | a member of VirtualSMC that provides used for monitoring fan speed.|
[SMCLightSensor](https://github.com/acidanthera/VirtualSMC) | a member of VirtualSMC that provides used for the ambient light sensor on laptops.|
[WhateverGreen](https://github.com/acidanthera/WhateverGreen) | Various patches necessary for certain ATI/AMD/Intel/Nvidia GPUs. This is needed for Intel UHD 620.|  
[AppleALC.kext](https://github.com/acidanthera/AppleALC) | An open source kernel extension enabling native macOS HD audio for not officially supported codecs without any filesystem modifications.|
[NVMeFix](https://github.com/acidanthera/NVMeFix) | NVMeFix is a set of patches for the Apple NVMe storage driver, IONVMeFamily.|
[CPUFriend](https://github.com/acidanthera/CPUFriend) | A Lilu plug-in for dynamic power management data injection.|
[CPUFriendDataProvider](https://github.com/corpnewt/CPUFriendFriend) | A CPUFriend plug-in for CPU power management.| 
[VoodooPS2Controller](https://github.com/acidanthera/VoodooPS2) | Contains updated Voodoo PS/2 Controller, improved PS2 Keyboard & Synaptics TouchPad.| 
[VoodooI2C](https://github.com/VoodooI2C/VoodooI2C) | Attaches to I2C controllers to allow plugins to talk to I2C trackpads.|
[VoodooI2CHID](https://github.com/VoodooI2C/VoodooI2C) | Can be used with I2C/USB Touchscreens and Trackpads.|
[BrightnessKeys](https://github.com/acidanthera/BrightnessKeys) | Automatic handling of brightness keys based on ACPI Specification.|
[RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X) | OS X open source driver for the Realtek RTL8111/8168 family. |  
[RtWlanU](https://github.com/chris1111/Wireless-USB-OC-Big-Sur-Adapter) | USB Wi-Fi adapter. |  |  
[RtWlanU1827](https://github.com/chris1111/Wireless-USB-OC-Big-Sur-Adapter) | USB Wi-Fi adapter. |  |  
[HoRNDIS9.2](https://github.com/jwise/HoRNDIS) | Android USB Tethering. |   
[UTBMap](https://github.com/USBToolBox/tool) | Kext to inject mapped USB ports |  
[USBToolBox](https://github.com/USBToolBox/kext) | Kext on UTBMap |
  
## SSDT Used
SSDT | Info | Status
:---------|:---------|:---------
[SSDT-GPI0](https://dortania.github.io/Getting-Started-With-ACPI/Laptops/trackpad-methods/manual.html) | Enable Trackpad I2C on MacOS. | Functional
[SSDT-NoHybGfx](https://dortania.github.io/Getting-Started-With-ACPI/Laptops/laptop-disable.html#bumblebee-method) | Disable dGPU on MacOS. | Functional
[SSDT-EC and SSDT-USBX](https://dortania.github.io/Getting-Started-With-ACPI/Universal/ec-fix.html#fixing-embedded-controller-ssdt-ecusbx) | Adds a fake Embedded Controller (SSDT-EC) and enables USB Power Management (SSDT-USBX). | Functional
[SSDT-HPET](https://dortania.github.io/Getting-Started-With-ACPI/Universal/irq.html#fixing-irq-conflicts-ssdt-hpet-oc-patches-plist) | Fixes IRQ conflicts. Required for on-board sound to work. | Optional
[SSDT-PLUG](https://dortania.github.io/Getting-Started-With-ACPI/Universal/plug.html#fixing-power-management-ssdt-plug) | Allow the kernel's XCPM(XNU's CPU Power Management) to manage CPU's power management. | Functional
[SSDT-PNLF](https://dortania.github.io/Getting-Started-With-ACPI/Laptops/backlight.html) | Adds Backlight Control for Laptop Screens. | Functional
[SSDT-SBUS-MCHC](https://dortania.github.io/Getting-Started-With-ACPI/Universal/smbus.html) | Fixes System Management Bus and Memory Controller in macOS. | Functional
[SSDT-RTCAWAC](https://dortania.github.io/Getting-Started-With-ACPI/Universal/awac.html) | SSDT-AWAC tries to re-enable the old RTC clock that is compatible with macOS, while SSDT-RTC0 will instead create a "fake" RTC clock if there is no legacy one to enable. | Functional
[SSDT-ALS0](https://github.com/Acidanthera/OpenCorePkg/blob/master/Docs/AcpiSamples/Source/SSDT-ALS0.dsl) | Enabling Ambient Light Sensor with macOS 10.15 or later. | Optional
[SSDT-Disable_WiFi_RP10](https://github.com/Nguyen12345tt/OpenCore-HP-15s-du1040tx-hackintosh/blob/main/ACPI/SSDT-Disable_WiFi_RP10.aml) | Disabling unsupported Wi-Fi Card on MacOS. | Optional

## boot-args Used
boot-arg | Info
:---------|:---------
-v | Enables verbose.
debug=0x100 | This disables macOS's watchdog which helps prevents a reboot on a kernel panic.
keepsyms=1 | This is a companion setting to debug=0x100 that tells the OS to also print the symbols on a kernel panic.
alcid=xxx | Used for setting layout-id for AppleALC, see [supported codecs](https://github.com/acidanthera/applealc/wiki/supported-codecs) to figure out which layout to use for your specific system. More info on this is covered in the [Post-Install Page](https://dortania.github.io/OpenCore-Post-Install/). |
igfxonln=1 | Forces all displays online, useful for resolving screen wake issues in 10.15.4+ on Coffee and Comet Lake.
-igfxblr | Fix backlight registers on KBL, CFL and ICL platforms.
-vi2c-force-polling | Enable I2C trackpad.

## Changelog

<details>
<summary>2024-12-30</summary>

- <b>Added</b>
  - Kernel
    - Add
      - RtWlanU: USB Wi-Fi Adapter for macOS.
      - RtWlanU1827: USB Wi-Fi Adapter for macOS.
- <b>Changed</b>
  - Kernel
    - Add
      - NVMEFix: Because macOS not supported.
  - NVRAM
    - 7C436110-AB2A-4BBB-A880-FE41995C9F82
      - csr-active-config
        - 03080000 for USB Wi-Fi Adapter.
- <b>Removed</b>
  - ACPI
    - Add
      - SSDT-Disable-WiFi-RP05.aml: Disable WiFi-card unsupported.
  - Kernel
    - Add
      - USBToolBox
      - UTBMap
</details>  

## Installation Steps

### Downloading OSX Image
- Click to OneDrive link and download it.
  - [Seoquia](https://drive.google.com/file/d/1ro8m1TrNJXmcWPsZOnEDKavu-gqhJm3l/view)
  - [Sonoma](https://drive.google.com/file/d/1QwXaDNc-YXUEEJxK2V1TewL5ZsfsE2UB/view)
  - [Ventura](https://drive.google.com/file/d/1QjbxYWEWK45FCbi8EUJj3skgocEKJVj7/view)
  - [Monterey](https://drive.google.com/file/d/1D2qMqzDi72akHkLBa6r1EKT_DXHIDs47/view)
  - [Big Sur](https://drive.google.com/file/d/1uP9ixgsrsFxUl55yTi_fOoG025rYR5gf/view)
  
### Writing OSX Image
- Download DMG file on link.
- Download [balenaEtcher](https://www.balena.io/etcher/).
- Open program and click to `Flash from file`.
- Select the OSX image `.dmg` file from the popup window.
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
    - VT-x(Virtualtion Technology)

      
## Credits
  
 - [Dortania](https://dortania.github.io) for developing OpenCore.
 - [Apple](https://www.apple.com) for macOS.
 - [Acidanthera](https://github.com/acidanthera) for most of the kexts.
 - [Hackintosh Việt Nam - OpenCore](https://www.facebook.com/groups/hackintosh.vietnam) for fix error to install MacOS.
 - And anyone else that helped to develop and improve hackintoshing.
