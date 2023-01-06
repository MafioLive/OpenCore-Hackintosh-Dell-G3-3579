## Install Guide for the Dell G3 3579 (i7-8750H) Model

## Introduction

This guide will walk you through downloading macOS, creating a bootable USB drive, and installing macOS on your Dell G3 3579 (i7-8750H) model. This guide is for the i7-8750H, GTX1050TI, no USB Type-C version of Dell G3 3579. If you have a different model, please refer to the [Dortania Guide](https://dortania.github.io/OpenCore-Install-Guide/).

## Prerequisites

Download the latest supported (0.8.8) release of OpenCore [here](https://github.com/acidanthera/OpenCorePkg/releases/tag/0.8.8).

Download the latest release of this repo [here](https://github.com/MafioLive/OpenCore-Hackintosh-Dell-G3-3579/releases/tag/5.0).

Get a USB drive with at least 8GB of space.

python 3.7 or higher (for creating the bootable USB drive)

## Downloading macOS

Extract and open the OpenCore folder.

Using the command prompt Navigate to Utilities > macrecovery

When in the macrecovery directory run the following command depending on the macOS version you want to install:

```

# Big Sur (11)

python3 macrecovery.py -b Mac-42FD25EABCABB274 -m 00000000000000000 download

# Monterey (12)

python3 macrecovery.py -b Mac-FFE5EF870D7BA81A -m 00000000000000000 download

# Latest version

# ie. Ventura (13)

python3 macrecovery.py -b Mac-4B682C642B45593E -m 00000000000000000 download

```

This will create a folder called com.apple.recovery.boot in the macrecovery directory.

## Creating the Bootable USB Drive

We will be using disk management to create the bootable USB drive. for other methods see the [Dortania Guide](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/windows-install.html#making-the-installer).

Open the disk management tool by pressing Windows Key + R and typing diskmgmt.msc

Right click on the USB drive and select **Format**

Set the volume label to **EFI**
The file system should be **FAT32**

Make sure quick format is **checked**

Then click **OK**

## Setting up the Bootabel USB Drive

Extract the efi folder downloaded from the latest release of this repo.

Copy the efi folder to the root of the USB drive.

Copy the com.apple.recovery.boot folder from macrecovery to the root of the USB drive.

## Setting up the BIOS

Restart your computer and enter the BIOS by pressing F2.

Change the following settings:

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

Apply then save and exit.

## Installing macOS

Restart your computer and enter the Boot picker by pressing F12.

Select the USB drive and press enter.

Select the option EFI (DMG) and press enter.

wait until the macOS recovery screen appears.

Select Disk Utility

Select the disk you want to install macOS on.

Format the disk as APFS, once complete exit Disk Utility.

Select Reinstall macOS

eventually the macOS will restart and you will be presented with the apple logo with a timer underneth it.

Once the timer is done, you will be presented with the macOS setup screen.

## Finished

Congratulations you now have macos setup on your Dell G3 3579.
