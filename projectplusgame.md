# P+ USB Drive Setup

## Create Partitions
- Windows 11: **Disk Management** (built-in)
- macOS 15 Sequoia
  - [iPartition](https://coriolis-systems.com/) to delete existing partition and create *first partition* and *second partition* (both FAT32)
  - **Disk Utility** (built-in) to reformat *second partition* to exFAT
- Ubuntu 24.04.2 LTS (Noble Numbat): **Disks** (built-in)
  - You'll probably need to run `sudo apt install exfat-fuse` to enable exFAT

## Format *First Partition* to WBFS
- Windows 11: [Wii Backup Manager](https://wiibackupmanager.co.uk/)
- Non-Windows: [CfgUSBLoader](https://github.com/nitraiolo/CfgUSBLoader/releases/latest)
  1. Press A to select device
  2. Press A to select *first partition*
  3. Press R to format WBFS
  4. Press A to confirm
  5. Press Start to exit

## Copy Brawl ISO
- Windows 11: [Wii Backup Manager](https://wiibackupmanager.co.uk/)
- macOS: [Wiimms WBFS Tool](https://wit.wiimm.de/download.html) -
Unfortunately, the current Mac binaries are not built correctly. You'll have to do some manual steps to make it work:
  1. Unzip and install `sudo sh install.sh`
  2. Remove ARM part of universal binary `lipo -remove arm64 /usr/local/bin/wwt -output /usr/local/bin/wwt`
  3. Copy (supports ISO, WDF, WIA, CISO, WBFS, GCZ and FST) `sudo wwt add --source ~/Downloads/RSBE01.iso --auto --progress`
- Linux: [Wii Backup Fusion](https://github.com/larsenv/Wii-Backup-Fusion/releases/latest)
