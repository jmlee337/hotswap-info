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
- macOS/Linux: [Wii Backup Fusion](https://github.com/larsenv/Wii-Backup-Fusion/releases/latest)
  - On macOS you'll need to follow the directions to [open an app from an unidentified developer](https://support.apple.com/en-gb/guide/mac-help/mh40616/mac).
