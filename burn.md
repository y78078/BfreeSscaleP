# Burn

## Linux 4.1.15
### Android
echo 0 > /sys/block/mmcblk%mmc%boot0/force_ro

dd if=/dev/zero of=/dev/block/mmcblk%mmc%boot0 bs=512 seek=2
## Linux 4.1.33
### Yocto
echo 0 > /sys/block/mmcblk%mmc%boot0/force_ro

dd if=/dev/zero of=/dev/mmcblk%mmc%boot0 bs=512 seek=2

## Linux 3.14.52
adb shell  "echo 56 > /sys/block/mmcblk3/device/boot_config"

adb shell  dd if=/dev/zero of=/dev/block/mmcblk3 bs=1024 count=10240

## Linux 4.19.35
### Android
echo 0 > /sys/block/mmcblk%mmc%boot0/force_ro

dd if=/dev/zero of=/dev/block/mmcblk%mmc%boot0 bs=512 seek=2

### Yocto
echo 0 > /sys/block/mmcblk%mmc%boot0/force_ro

dd if=/dev/zero of=/dev/mmcblk%mmc%boot0 bs=512 seek=2

#### flash.bin (m4&scu) into imx-image.rootfs.wic.bz2
decompress imx-image.rootfs.wic.bz2 to imx-image.rootfs.wic

sudo dd if=flash.bin of=imx-image.rootfs.wic bs=1k seek=32 conv=notrunc

compress imx-image.rootfs.wic to imx-image.rootfs.wic.bz2

### flash to sdcard
bzcat imx-image.rootfs.wic.bz2 | sudo dd of=/dev/sdX bs=1M conv=fsync
