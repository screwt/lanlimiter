# Lan/Wan bandwith limiter

## Test with 200 kbits/s download and 20 kbits/s upload limit (local lan bandwith is not affected)
```shell
sudo ./wondershaper eth0 2000 200
```
see var LAN_SUBNET, line 42 to specifiy your local net mask

## Automatic limitation, add the fallowing lines to  /etc/network/interfaces
up /usr/sbin/wondershaper <interface réseau> <downspeed> <upspeed>
down /usr/sbin/wondershaper clear <interface réseau>


## Based on that page:
 * http://ideatrash.net/2014/07/making-wondershaper-play-nice-on-lan.html
 * https://doc.ubuntu-fr.org/qos
 