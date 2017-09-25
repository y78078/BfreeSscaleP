# Burn

## Linux 4.1.33
echo 0 > /sys/block/mmcblk%mmc%boot0/force_ro

dd if=/dev/zero of=/dev/mmcblk%mmc%boot0 bs=512 seek=2

## Linux 3.14.52
adb shell  "echo 56 > /sys/block/mmcblk3/device/boot_config"

adb shell  dd if=/dev/zero of=/dev/block/mmcblk3 bs=1024 count=10240

