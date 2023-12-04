This proyect is based on @Aleixsr GitHub's Repository

## Install macOS from Windows following the next steps

### Device Info

| Components   |             INFO               |
|--------------|--------------------------------|
|     CPU      |   Intel Comet Lake i7-10710u   |
|     RAM      |          (1 x 16GB)            |
|     IGPU     |   Intel Graphics UHD 630       |
|     DGPU     |    Nvidia GTX1650 Max-Q        |
|    NVMe 1    |         Crucial 1TB            |
|    Audio     |       Realtek ALC298           |
|   Wireless   |         Intel AX201            |

### What Doesn't Work

- Nvidia GTX1650 Max-Q (Disabled via SSDT)
- Fingerprint Reader
- Card Reader Realtek (SD Slot)

### Instructions for Use

- Download my EFI folder
- Download [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)
- Execute GenSMBIOS and select Install MacSerial and press ok, then select Generate SMBIOS and introduce: 'MacBookPro15,4'
- Paste the codes on the config.plist of the Serial -> SystemSerialNumber, Board Serial -> MLB, SmUUID -> SystemUUID (like the image bellow)

![Fill the Gaps](./example_images/Fill%20the%20gaps%20with%20gensmbios%20info.png)

- click ctrl + R, ctrl + sift + R, accept and save the config.plist.

### Copy the EFI to your pendrive

- Make sure you have 2 folders:
- The EFI you just download and modify
- Another folder named: *'com.apple.recovery.boot'*

*Note: It is important that you make sure that you install at first Catalina, once you finish the installation, you can upgrade the macOS version natively.*

- Now, download *Catalina* version of macOS following the [Dothania official](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/windows-install.html#downloading-macos), and move the **BaseSystem.chunklist** and the **BaseSystem.dmg** to the **'com.apple.recovery.boot'** folder.

![USB Folders](./example_images/USB%20Folders.png)

### Prepare the BIOS

Access the BIOS by rebooting your PC and while the MSI logo appears, you must PRESS the SUPR button, that will lead you to a blue screen.

- To unlock the hidden features, Press L-ALT + R-CTRL + R-SHIFT + F2 or (fn + F2)
- Then, go to: Advanced -> Power & Performance -> CPU - Power Management Control -> CPU Lock Configuration -> CFG Lock : **Disabled**

### How To Boot the Hackintosh

- Insert your pendrive and reboot your pc, then hold F11 or (FN + F11) and select your USB with the macOS Installer.
- It will start the installation and will appear the apple logo
- You will log into the macOS installer.
- Go to disk utility, show all devices and erase the disk where you want macOS with APFS format and GUID Map.
- Connect to your wifi and start the installation in the disk you previously erased.
- Your PC will reboot several times.

### Post Installation

- Download [Mount EFI](https://github.com/corpnewt/MountEFI), and run the **.command**, select the disk where you have install macOS.
- It wiil appear an EFI folder in your Finder's sidebar, copy the EFI folder of your USB in your Finder's sideba