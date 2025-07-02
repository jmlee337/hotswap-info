# P+ USB Drive Setup
When using also USB drives for P+, the recommended method of formatting as FAT32 can cause problems for hotswap.
This is because Slippi Nintendont struggles and often fails to write to FAT32 drives that are more than about 50% full.
If you want to use the same USB drives for P+ and hotswap I recommend creating separate partitions:
- *First partition* formatted as WBFS for P+ and other Wii ISOs
- *Second partition* formatted as exFAT for hotswap

When set up this way, Project+ USB Loader will see only *first partition* and Slippi Nintendont/Replay Manager for Slippi will see only *second partition*.
This is easiest to set up using Windows, but is also possible on macOS and Linux.

## Create Partitions
*First partition* can have any format or none as we'll be changing it to WBFS, but make sure it is at least 7.3 GB for Brawl ISO.
*Second partition* can be nearly any size, 256 MB should be enough for any hotswap situation.
- Windows 11: **Disk Management** (built-in)
- macOS 15 Sequoia
  - [iPartition](https://coriolis-systems.com/) to delete existing partition and create *first partition* and *second partition* (both FAT32)
  - **Disk Utility** (built-in) to reformat *second partition* to exFAT
- Ubuntu 24.04.2 LTS (Noble Numbat): **Disks** (built-in)
  - You'll probably need to run `sudo apt install exfat-fuse` to enable exFAT

## Format *First Partition* to WBFS
- Windows 11: [Wii Backup Manager](https://wiibackupmanager.co.uk/)
  - **MAKE SURE YOU SELECT YOUR USB DRIVE *FIRST PARTITION* AND NOT ANY INTERNAL HARD DRIVES**
- Non-Windows: [CfgUSBLoader](https://github.com/nitraiolo/CfgUSBLoader/releases/latest) on Wii
  1. Press A to select device
  2. Press A to select *first partition*
  3. Press R to format WBFS
  4. Press A to confirm
  5. Press Start to exit

## Copy Brawl ISO
- Windows 11: [Wii Backup Manager](https://wiibackupmanager.co.uk/)
- macOS/Linux: [Wiimms WBFS Tool](https://wit.wiimm.de/download.html)
(You should also be able to use this to format *first partition* to WBFS, but I did not try that)
  1. Unzip and install `sudo sh install.sh`
  2. On **Mac only** fix the binary to actually run `lipo -remove arm64 /usr/local/bin/wwt -output /usr/local/bin/wwt`
  3. Copy (supports ISO, WDF, WIA, CISO, WBFS, GCZ and FST) `sudo wwt add --source ~/Downloads/RSBE01.iso --auto --progress`
