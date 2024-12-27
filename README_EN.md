
## ASUS X455LAB WX668D OpenCore Hackintosh

***OpenCore EFI for ASUS X455LAB***

[![](https://img.shields.io/badge/Repository-JaemanPratama-informational?style=flat&logo=apple&logoColor=white&color=9debeb)](https://github.com/JaemanPratama)
[![](https://img.shields.io/badge/Telegram-HackintoshLover-informational?style=flat&logo=telegram&logoColor=white&color=5fb659)](https://t.me/HackintoshLover)
[![](https://img.shields.io/badge/Facebook-HackintoshIndonesia-informational?style=flat&logo=facebook&logoColor=white&color=3a4dc9)](https://www.facebook.com/groups/hackintosh.indonesia)

> :warning: **WARNING:**
This is not a plug-and-play EFI guide. Refer to [Dortania](https://dortania.github.io/getting-started/) before proceeding. I am not responsible for any damage. This OpenCore configuration is optimized for my specific hardware. Use it only as a reference or if you have the same/similar hardware.

![System Preview](https://user-images.githubusercontent.com/89202419/166002855-8d96a3a2-bc06-4173-80f5-3c17eadb5c23.png#gh-light-mode-only)

---

```
By using this EFI, you agree to take all risks associated with its use.
It may be unstable for your laptop.
I am not responsible for any damage caused by using this EFI.
USE AT YOUR OWN RISK!
```

---

### :mag_right: Quick Access
- [ACPI Collection](https://github.com/JaemanPratama/Hackintosh-Asus-X455LAB-SERIES/tree/main/ACPI)
  - [Hotpatch ACPI OpenCore](https://github.com/jsassu20/OpenCore-HotPatching-Guide)
  - [Dortania Patch SSDT Guide](https://dortania.github.io/Getting-Started-With-ACPI/ssdt-methods/ssdt-easy.html)
- [Enable Touchpad Features](https://github.com/JaemanPratama/Hackintosh-Asus-X455LAB-SERIES/tree/main/Aktifkan%20Fitur%20Touchpad)
  - [Original Guide](https://osxlatitude.com/forums/topic/5966-details-about-the-smart-touchpad-driver-features/)
- [Dual Boot With Windows 10/11](https://github.com/JaemanPratama/Hackintosh-Asus-X455LAB-SERIES/tree/main/Dual%20Boot%20Windows%2010)
- [Hackintosh Tools](https://github.com/JaemanPratama/Hackintosh-Asus-X455LAB-SERIES/tree/main/Hackintosh%20Tools)
- [About Keyboard](https://github.com/JaemanPratama/Hackintosh-Asus-X455LAB-SERIES/tree/main/Keyboard)
- [Quick Hackintosh Installation Guide](https://github.com/JaemanPratama/Hackintosh-Asus-X455LAB-SERIES/tree/main/Panduan%20Instalasi)
  - [Dortania’s Original Guide](https://dortania.github.io/OpenCore-Install-Guide/)
- [Post-Installation](https://github.com/JaemanPratama/Hackintosh-Asus-X455LAB-SERIES/tree/main/Post%20Installation)
  - [More Details](https://dortania.github.io/OpenCore-Post-Install/)
- [Benchmark Test Results](https://github.com/JaemanPratama/Hackintosh-Asus-X455LAB-SERIES/tree/main/Score%20Test%20Benchmark)

---

### ⚙️ Hardware Specifications

| **Category**   | **Component**                |
|----------------|-----------------------------|
| **Model**      | ASUS X455LAB WX668D         |
| **Processor**  | 2.0GHz Intel Core i3-5005U  |
| **Graphics**   | Intel HD 5500               |
| **RAM**        | 4 + 2 GB DDR3 1600 MHz      |
| **Storage**    | 256 GB MidasForce SATA SSD  |
| **Display**    | 14-inch HD LED (1366x768)   |
| **Wi-Fi/BT**   | Qualcomm Atheros AR9565     |
| **Ethernet**   | Realtek RTL8111             |
| **Audio**      | Conexant CX20751/2          |
| **Input**      | PS2 Keyboard & ETD0108 Touchpad |

[**ASUS X455LA User Manual (PDF)**](https://www.asus.com/id/supportonly/x455la/helpdesk_manual/?model2Name=X455LA)

---

### 🔊 Audio and Video Features

| Feature                              | Status | Dependency          |
|-------------------------------------|-------|--------------------|
| Full Graphics Acceleration (QE/CI)  | ✅   | `WhateverGreen.kext` |
| HDMI Port                           | ✅   | `WhateverGreen.kext` |
| Internal Camera                     | ✅   | `SSDT-HCK.aml`       |
| Internal DVD                        | ✅   | `SSDT-HCK.aml`       |
| Audio Recording                     | ✅   | `AppleALC.kext` with Layout ID = 28 |
| Audio Playback                      | ✅   | `AppleALC.kext` with Layout ID = 28 |

---

### 💡 Power Management

| Feature               | Status | Dependency           |
|-----------------------|--------|----------------------|
| Battery Percentage    | ✅      | `ECEnabler.kext`     |
| Hibernate             | ✅      | OpenCore Patches     |

---

### 🖥 Display, Touchpad, and Keyboard

| Feature                | Status | Dependency               |
|-----------------------|--------|--------------------------|
| Brightness Control    | ✅      | `WhateverGreen.kext`     |
| Built-in Keyboard     | ✅      | `ApplePS2SmartTouchPad.kext` |
| FN Keys               | ✅      | `AsusFnKeys.kext`        |

---

### 🔆 macOS Exclusive Features

| Feature              | Status | Dependency                 |
|---------------------|--------|----------------------------|
| iCloud, iMessage    | ✅      | Apple ID and SMBIOS setup  |
| Time Machine        | ✅      | Built-in                  |

---

### ☹️ Not Working
- **Airdrop**: Not compatible with Atheros Wi-Fi.
- **Gestures**: Stuck in mouse emulation mode.
- **Card Reader**: Not tested.

---

### Supported macOS Versions
- **Recommended**: Mojave, Catalina, Big Sur, Monterey.
- **Not Supported**: Ventura (Broadwell CPUs are unsupported).

---

### 🔍 BIOS Configuration
- Disable **Secure Boot**.
- Enable **Intel Virtualization** and **VT-d**.
- Set **DVMT Pre-Allocation** to `64M`.
- SATA Mode: `AHCI`.

---

### 💪 Upgrades
- Upgrade HDD to SSD for better performance.

---

### 🔑 Important Additional Notes About Hackintosh Process:

- **Do not follow YouTube videos**: They are often outdated and provide incorrect information.
- **Avoid prebuilt EFIs**: Prebuilt EFIs by other users may not match your system and can cause instability. Always configure your own EFI tailored to your system.
- **Do not use macOS distros**: Always download macOS directly from Apple's servers using Dortania's guide. Distros are often outdated, pirated, modified, or contain malware.
- **Use OpenCore over Clover**: Clover is considered obsolete, bloated, and not recommended anymore.

#### Summary:
1. Avoid YouTube guides.
2. Do not use prebuilt EFIs from others.
3. Always download macOS directly from Apple, not from other sources.
4. Stop using Clover; use OpenCore instead.

---

### 🤝 Acknowledgements:
Special thanks to the following contributors and resources:
- [Acidanthera](https://github.com/acidanthera)
- [Rehabman](https://github.com/RehabMan)
- [EmlyDinesh](https://github.com/EMlyDinEsHMG)
- [InsanelyMac](https://www.insanelymac.com)
- [Olarila](http://olarila.com)
- [OSXLatitude](https://osxlatitude.com)
- [Hackintosh Lover](https://t.me/HackintoshLover)
- [Hackintosh Indonesia](https://id-id.facebook.com/groups/hackintosh.indonesia/)
- [asepms92](https://github.com/asepms92)
- [zacharyrs](https://github.com/zacharyrs/GL551JW-Hackintosh)
- [Google](https://google.com)
- [Reddit](https://www.reddit.com/r/hackintosh/)
- And many other developers.
