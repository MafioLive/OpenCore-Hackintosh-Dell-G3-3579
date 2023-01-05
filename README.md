# OpenCore Hackintosh for Dell G3 3579

[![macOS](https://img.shields.io/badge/macOS-11.7.2-orange)](https://www.apple.com.cn/macos/big-sur-preview/)
[![OpenCore](https://img.shields.io/badge/OpenCore-0.8.8-9cf)](https://github.com/acidanthera/OpenCorePkg)
[![license](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)

<img align="right" src="https://support.apple.com/content/dam/edam/applecare/images/en_US/macos/psp-mini-hero-macos-high-sierra-whats-new_2x.png" alt="Critter" width="250">

### Latest Release: [v5.0](https://github.com/MafioLive/OpenCore-Hackintosh-Dell-G3-3579/archive/refs/heads/master.zip)

**macOS Version: 11.7.2**

**OpenCore Version: [0.8.8 Official](https://github.com/acidanthera/OpenCorePkg/releases/tag/0.8.8)**

**The continuation of this project would not have been made possible without [Tonyleelyy](https://www.github.com/tonyleelyy)**

This OpenCore hackintosh repo is made for i7-8750H, GTX1050TI, no USB Type-C version of Dell G3 3579.


## Updates

2023-01-05

OC 0.8.8 + Kexts Updated.


## Configuration

| Specifications | Detail | Working |
| :------------: | :------: | :--------: |
| Model | Dell G3 3579 | ✅ |
| Processor | Intel Core i7-8750H @ 2.20Ghz | ✅ |
| Memory | 16GB Micron DDR4 2666Mhz | ✅ |
| SSD | BC501 NVMe SK hynix 128GB | ✅ |
| HDD | WD10SPZX 1TB | ✅ |
| iGPU | Intel UHD Graphics 630 | ✅ |
| dGPU | NVIDIA GeForce GTX 1050 TI 4G | 🚫 |
| Sound Card | Realtek ALC236 | ✅ |
| Ethernet Card | Realtek RTL8111 | ✅ |
| Wireless Card | Inte Wireless-AC 9462 | ✅ |

## BIOS Configuration

| **System Configuration** |      |
| ------- | ---|
| SATA Operation       | AHCI |
|                      |      |
| **Secure Bootxu**   |      |
| Secure Boot Enable   | Disabled (Uncheck) |
|  |                    |
| **Intel Software Guard Extensions** |                    |
| Intel SGX Enable | Disabled           |
|  |                    |
| **POST Behavior** |                    |
| Fastboot | Thorough           |
|  |                    |
| **Virtualization Support** |                    |
| VT for Direct I/O | Disabled (Uncheck) |

Please update BIOS to the newest version.

Everything else is set default.

## Working

- macOS 11.7.2
- CPU (Boost to 4.0Ghz)
- iGPU
- Ethernet
- Audio (Layout=15)
- USB (Customed by USBPorts.kext)
- Trackpad
- WebCam
- Bluetooth (With On/Off buttom)
- Wi-Fi (Supported by [AirportItlwm](http://bbs.pcbeta.com/viewthread-1848662-1-1.html))

## Not Working

- dGPU (Disabled by SSDT)
- HDMI (Directly link to dGPU)
- Internal SD Card Reader
