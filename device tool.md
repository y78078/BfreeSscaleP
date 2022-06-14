# tool

## sound
/sys/class/sound/

## backlight
/sys/class/backlight/backlight

echo 44 > brightness

## fb mode
/sys/class/graphics/fb0/mode

/sys/class/graphics/fb0/modes

## i2c axis-accelerometer / gsensor

/sys/bus/i2c/devices

/sys/bus/iio/devices/iio:device0

cat /dev/iio:device0 | hexdump

# GPIO RS232

echo 4 > /sys/class/gpio/export

echo 5 > /sys/class/gpio/export

echo 16 > /sys/class/gpio/export

echo out > /sys/class/gpio/gpio5/direction
echo out > /sys/class/gpio/gpio16/direction
echo 1 > /sys/class/gpio/gpio16/active_low

# USB host & device change
1. kernel config

Device Drivers  --->

    [*] USB support  --->

          -*-   USB Role Switch Support

CONFIG_USB_ROLE_SWITCH: 

USB Role Switch is a device that can select the USB role - host or        

device - for a USB port (connector). In most cases dual-role capable    

USB controller will also represent the switch, but on some platforms   

multiplexer/demultiplexer switch is used to route the data lines on    

the USB connector between separate USB host and device controllers.

2. code

drivers/usb/roles/

class.c  intel-xhci-usb-role-switch.c  Kconfig  Makefile

3. user space(sysfs)

switch usb role mode, base on cdns3 usb.

first, we need to configure dr_mode = "otg" in dts, and enable CONFIG_USB_CDNS3_GADGET and CONFIG_USB_CDNS3_HOST in kernel config.

/sys/class/usb_role/

echo device > /sys/class/usb_role/400000.usb-role-switch/role

echo host > /sys/class/usb_role/400000.usb-role-switch/role
