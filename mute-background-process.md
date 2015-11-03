# Mute background process

[Ref](http://unix.stackexchange.com/questions/26534/how-to-dev-null-background-processes-informational-output)
Command excuted in background wil output pid and info after done. This can be muted by
```
( command &) > /dev/null 2>&1
```
