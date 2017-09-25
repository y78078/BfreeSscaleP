# Burn

## Linux 3.14
echo 0 > /sys/block/mmcblk%mmc%boot0/force_ro
dd if=/dev/zero of=/dev/mmcblk%mmc%boot0 bs=512 seek=2

## Linux 4.1
