# Getting on the Hall E network

1. `git clone git://github.com/cjdelisle/cjdns.git`
2. `cd cjdns && ./do`
3. `./cjdroute --genconf >> ~/cjdroute.conf`
4. `ed ~/cjdroute.conf` (Use your editor of choice)

```
    /* <-- Remove me
     "ETHInterface": [
         ... "bind": "wlan0", <-- This should be wlan0, not eth0
     */  <-- and me
```
<!-- this is needed for the syntax highlighting -->

5. Connect your wlan device to the `cjdns` adhoc network (at this point you will be off the net)
6. `sudo ./cjdroute < ~/cjdroute.conf` (root is needed because you're binding a raw socket)
7. `sudo bash -c "echo 'nameserver fc38:4c2c:1a8f:3981:f2e7:c2b9:6870:6e84' > /etc/resolv.conf"`
8. `irssi -c irc.hypeirc.net`
9. `/join #hyperboria`
