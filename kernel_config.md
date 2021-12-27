# Yocto bitbake kernel

## sudo apt-get install
## bitbake linux-imx -c menuconfig

## Linux發行版自帶usb to serial驅動，以模組方式編譯驅動，在核心原始碼目錄下執行Make MenuConfig選擇Devces drivers-->USB seupport--> <M>USB Serial Converter support --> <M> USB driver for GSM and CDMA modems & [*]USB Generic Serial Driver
https://www.itread01.com/content/1546198939.html

https://blog.csdn.net/u010356768/article/details/105792928

https://stackoverflow.com/questions/52499588/yocto-bitbake-config-file-location
