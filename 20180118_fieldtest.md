# Field test

## prepare
cp wvdial.conf
cp wpa_supplicant.conf
delay 

## AT command

at+csq
at+cops?
at+qcfg="band",d3,80,0
at+qnwinfo
atd09XXXXXXXX;
ata
ath

## wifi test
iperf3 -c IP -t 20 -i 1

## wifi setting
route add -net 0.0.0.0 gw 192.168.31.1 mlan0
wpa_supplicant -B -i mlan0 -c /etc/wpa_supplicant.conf
