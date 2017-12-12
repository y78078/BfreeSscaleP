# BSP rootfs release manual pack step

## 1. add getty@ttyGS0.service to /etc/systemd/system/getty.target.wants/
## ln -s ../../../../lib/systemd/system/getty@.service
## edit /lib/systemd/system/serial-getty@.servicecd ../
## add fonts to /usr/lib/fonts
## edit /etc/profile
## mkdir /home/root/.conf
## add scout.conf

