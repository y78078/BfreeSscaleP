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
