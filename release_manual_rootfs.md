# BSP rootfs release manual pack step

## 1. add getty@ttyGS0.service to /etc/systemd/system/getty.target.wants/
## remove getty@tty1.service
## ln -s ../../../../lib/systemd/system/getty@.service
## edit /lib/systemd/system/serial-getty@.service
## add fonts to /usr/lib/fonts
## edit /etc/profile
## mkdir /home/root/.conf
## add scout.conf
## /etc/modprobe.d add quectel.conf options usbserial vendor=0x2c7c product=0x0125
## /etc/modules-load.d add g_serial.conf usbserial.conf
## add wvdial.conf

