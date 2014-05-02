EteroMAX
========

wifi polling concept for openwrt

registration, wpa, keys work as is

after connection client sends RTS to AP and wait.
AP roun-robin cliens, if it has data it sends it, after sends CTS to client and then client sends data to AP, *after* sending buffer it sends RTS.

If buffer larger than some threshhold it sends new RTS, if AP`s buffer lesser then threshhold it sends CTS to this client, else to next one.

It may be compatable with 802.11.
