# DNS flush

[Ref](https://www.91ri.org/3112.html)
[Ref](http://wangheng.org/linux-windows-mac-refresh-dns.html)

## ubuntu

```
/etc/init.d/nscd restart	# NSCD
rndc flush			# bind9utils
/etc/init.d/dnsmasq restart	# dnsmasq
```

```
/etc/init.d/dns-clean
```

## OS X

```
dscacheutil -flushcache
```
