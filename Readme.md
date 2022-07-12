## Recovery device tree for Samsung Galaxy Tab A7 Lite

## Compile tutorial

```sh
export ALLOW_MISSING_DEPENDENCIES=true
. build/envsetup.sh
lunch twrp_gta7litewifi-eng
make recoveryimage
```

## Status
Blocking checks
- [x] Correct screen/recovery size
- [x] Working Touch, screen note: touch not working after reboot
- [x] Backup to internal/microSD
- [x] Restore from internal/microSD
- [x] reboot to system
- [x] ADB



Medium checks
- [x] update.zip sideload
- [x] UI colors (red/blue inversions)
- [ ] Screen goes off and on
- [ ] F2FS/EXT4 Support, exFAT/NTFS where supported
- [ ] all important partitions listed in mount/backup lists
- [ ] backup/restore to/from external (USB-OTG) storage (not supported by the device)
- [ ] backup/restore to/from adb (https://gerrit.omnirom.org/#/c/15943/)
- [ ] decrypt /data
- [ ] Correct date


Minor checks
- [ ] MTP export
- [x] reboot to bootloader
- [ ] reboot to recovery
- [ ] poweroff
- [ ] battery level
- [ ] temperature
- [ ] encrypted backups
- [x] input devices via USB (USB-OTG) - keyboard, mouse and disks (not supported by the device)
- [ ] USB mass storage export
- [ ] set brightness note: display brightness work partially
- [ ] vibrate
- [ ] screenshot
- [ ] partition SD card

This device tree was made with the intention to help users with this device, blindly helped with the help of users owning the device.
It will boot, feel free to fork this and do whatever you want. Take this as a start point to port twrp to your device.
