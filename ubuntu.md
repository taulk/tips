# Ubuntu
## Get ubuntu version
```
uname [-a]
cat /etc/issue
cat /proc/version
cat /etc/lsb_release
lsb_release -a
```

## Sudo command no need of password
Change /etc/sudoers
```
%admin ALL=(ALL) ALL

%sudo     ALL=(ALL:ALL) ALL
```
to
```
%admin ALL=(ALL) NOPASSWD: NOPASSWD: ALL

%sudo     ALL=(ALL:ALL) NOPASSWD: NOPASSWD: ALL
```

## List installed app

[Ref](http://askubuntu.com/questions/17823/how-to-list-all-installed-packages)

```
# all packages
dpkg --get-selections
# simply
dpkg -l
# expressly installed (not installed as dependencies)
aptitude search '~i!~M'
# using apt-mark
apt-mark showauto
apt-mark showmanual
```

a typical workflow [Ref](http://jeffhoogland.blogspot.com/2012/08/howto-clone-all-programs-installed-via.html)

```
dpkg -l | awk '/^ii/ { print $2 }' >package-list
xargs apt-get install -y < package-list
```

## Refresh ip

Typically when you access vbox when host's ip changed.

```
ifdown {eth0}
ifup {eth0}
/etc/init.d/networking restart
```

## Measure network traffic

[Ref](http://serverfault.com/questions/107393/linux-how-to-measure-daily-montly-network-traffic)
[Ref](http://humdi.net/vnstat/)
[Ref](http://www.binarytides.com/linux-commands-monitor-network/)

```
vnstat
```

## Chat with nc

```
man nc
nc -l port
nc ip port
```
