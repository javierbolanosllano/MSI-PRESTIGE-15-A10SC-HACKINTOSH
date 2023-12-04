This proyect is based on @Aleixsr GitHub's Repo

## Install macOS from Windows - OPENCORE

## Device Info

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
- Navigate through the config.plist with ProperTree and...
- Go: Root -> PlatformInfo and paste 
- Copy the Serial -> SystemSerialNumber, Board Serial -> MLB, SmUUID -> SystemUUID (like the image bellow)
![Fill the Gaps](./images/Fill%20the%20gaps%20with%20gensmbios%20info.png)
