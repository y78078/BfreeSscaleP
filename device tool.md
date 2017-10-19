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
