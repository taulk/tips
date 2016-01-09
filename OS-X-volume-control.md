# Control Volume

## command line

[Ref](http://osxdaily.com/2007/04/28/change-the-system-volume-from-the-command-line/)
[Ref](https://coderwall.com/p/22p0ja/set-get-osx-volume-mute-from-the-command-line)


```
osascript -e "set Volume 0" # 10 is max

osascript -e 'output volume of (get volume settings)' # Get volume (0..100)
osascript -e 'set ovol to output volume of (get volume settings)'
osascript -e 'set volume output volume 50' # 100 is max

osascript -e 'output muted of (get volume settings)' # true or false
osascript -e 'set volume output muted true' # Set muted
```

## Apple Script

```
set currentVolume to output volume of (get volume settings)
set volume output volume (currentVolume + 5)
```

Save as 'Application'.

Bind a keyboard shortcut to the .app file.
