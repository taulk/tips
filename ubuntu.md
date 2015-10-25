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
