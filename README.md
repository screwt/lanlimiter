# Lan/Wan bandwith limiter

 * Test with 200 kbits/s download and 20 kbits/s upload limit (local lan bandwith is not affected)
```shell
sudo ./wondershaper eth0 2000 200
```
see var LAN_SUBNET, line 42 to specifiy your local net mask