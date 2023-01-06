# OpenCore Hackintosh for Dell G3 3579

[![macOS](https://img.shields.io/badge/macOS-13.1-green)](https://www.apple.com.cn/macos/big-sur-preview/)
[![OpenCore](https://img.shields.io/badge/OpenCore-0.8.8-9cf)](https://github.com/acidanthera/OpenCorePkg)
[![license](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)

<img align="right" src="https://i.pcmag.com/imagery/reviews/04iuiyBZ61YPzdVS4GfRYKM-29.fit_scale.size_1028x578.v1666629922.png" alt="Ventura Logo" width="250">

### Latest Release: [v5.0](https://github.com/MafioLive/OpenCore-Hackintosh-Dell-G3-3579/releases/tag/5.0)

**macOS Version: 13.1**

**OpenCore Version: [0.8.8 Official](https://github.com/acidanthera/OpenCorePkg/releases/tag/0.8.8)**

**The continuation of this project would not have been made possible without [Tonyleelyy](https://www.github.com/tonyleelyy)**

[**Install Guide**](https://github.com/MafioLive/OpenCore-Hackintosh-Dell-G3-3579/blob/a5b08d2c0a1e6c4b025d87c38de7626324c0b618/INSTALL-GUIDE.md)

This OpenCore hackintosh repo is made for i7-8750H, GTX1050TI, no USB Type-C version of Dell G3 3579.

## Updates

2023-01-05

- OC 0.8.8 + Kexts Updated.
- macOS 12.6.2 (Monterey) Now Supported.
- macOS 13.1 (Ventura) Now Supported

## Supported macOS Versions:

- macOS 13.1 (Ventura)
- macOS 12.6.2 (Monterey)
- macOS 11.7.2 (Big Sur)

## Configuration

| Specifications |            Detail             | Working |
| :------------: | :---------------------------: | :-----: |
|     Model      |         Dell G3 3579          |   ✅    |
|   Processor    | Intel Core i7-8750H @ 2.20Ghz |   ✅    |
|     Memory     |   16GB Micron DDR4 2666Mhz    |   ✅    |
|      SSD       |   BC501 NVMe SK hynix 128GB   |   ✅    |
|      HDD       |         WD10SPZX 1TB          |   ✅    |
|      iGPU      |    Intel UHD Graphics 630     |   ✅    |
|      dGPU      | NVIDIA GeForce GTX 1050 TI 4G |   🚫    |
|   Sound Card   |        Realtek ALC236         |   ✅    |
| Ethernet Card  |        Realtek RTL8111        |   ✅    |
| Wireless Card  |     Inte Wireless-AC 9462     |   ✅    |

## BIOS Configuration

| **System Configuration**            |                    |
| ----------------------------------- | ------------------ |
| SATA Operation                      | AHCI               |
|                                     |                    |
| **Secure Bootxu**                   |                    |
| Secure Boot Enable                  | Disabled (Uncheck) |
|                                     |                    |
| **Intel Software Guard Extensions** |                    |
| Intel SGX Enable                    | Disabled           |
|                                     |                    |
| **POST Behavior**                   |                    |
| Fastboot                            | Thorough           |
|                                     |                    |
| **Virtualization Support**          |                    |
| VT for Direct I/O                   | Disabled (Uncheck) |

Please update BIOS to the newest version.

Everything else is set default.

## Working

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
