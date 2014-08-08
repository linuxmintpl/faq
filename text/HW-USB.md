#Urządzenia USB, modemy, itd#
********************

## 1. Jak skonfigurować połączenie przez USB z routerem Huawei E5372?

Przełączenie urządzenia  wtryb NDIS:  
Polecenie (jako root):  
    **echo cho -e "AT^NDISDUP=1,1,\"internet\"\r" > /dev/ttyUSB0 && dhclient wwan0**

W wyniku powyższego polecenia powstanie interfejs __wwan0__.  
Sprawdź:
    wwan0     Link encap:Ethernet  HWaddr aa:bb:cc:dd:ee:ff  
              inet addr:192.168.8.XXX  Bcast:192.168.8.255  Mask:255.255.255.0
              inet6 addr: fe80::e5b:8fff:fe27:9a64/64 Scope:Link
              UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
              RX packets:5 errors:0 dropped:0 overruns:0 frame:0
              TX packets:64 errors:0 dropped:0 overruns:0 carrier:0
              collisions:0 txqueuelen:1000 
              RX bytes:1356 (1.3 KB)  TX bytes:862680 (862.6 KB) **
