# Lan/Wan bandwidth limiter

## Test with 200 kbits/s download and 20 kbits/s upload limit (local lan bandwidth is not affected)
```shell
sudo ./wondershaper eth0 2000 200
```
see var LAN_SUBNET, line 42 to specifiy your local net mask

## Automatic limitation, add the fallowing lines to  /etc/network/interfaces
```shell
up /usr/sbin/wondershaper <interface réseau> <downspeed> <upspeed>
down /usr/sbin/wondershaper clear <interface réseau>
```

## Based on these pages:
 * http://ideatrash.net/2014/07/making-wondershaper-play-nice-on-lan.html
 * https://doc.ubuntu-fr.org/qos
 