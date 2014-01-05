Raspberry Pi MediaTek MT7601
============================

Drivers for the MediaTek MT7601 USB Wifi adaptor.

```
3.10.25+
Linux raspberrypi 3.10.25+ #622 PREEMPT Fri Jan 3 18:41:00 GMT 2014 armv6l GNU/Linux
```

1. Copy mt7601Usta.ko to /lib/modules/3.10.25/kernel/drivers/net/wireless

2. Copy RT2870STA.dat to /etc/Wireless/RT2870STA directory

3. Run sudo depmod -a

4. Add the below text to /etc/network/interfaces. Note that quotes around SSID and password are required
```
auto ra0
allow-hotplug ra0
iface ra0 inet dhcp
wpa-ssid "ENTER YOUR NETWORK SSID"
wpa-psk "ENTER YOUR NETWORK PASSWORD"
```



References:

http://gowthamgowtham.blogspot.co.uk/2013/11/mediatekralink-wifi-adapter-in.html

http://www.raspberrypi.org/phpBB3/viewtopic.php?p=179845#p179845
