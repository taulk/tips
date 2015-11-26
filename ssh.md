# SSH

## Chain

local --> host1 --> host2

```
host1:$ ssh -ND port host2
local:$ ssh -NL port:localhost:port host1
```

## Spawn & Expect

```
#!/usr/bin/expect -f
spawn ssh usr@ip
expect "*assword"
send "password\r"
interact
```
