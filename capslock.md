# Change Caps Lock to Ctrl

[Ref](http://blog.yxwang.me/2009/05/caps-lock-to-ctrl/)
[Ref](http://efod.se/writings/linuxbook/html/caps-lock-to-ctrl.html)
[Ref](http://blog.yxwang.me/2010/10/change-caps-lock-state-by-software/)

## Windows

remapkey(xp).

SendKeys(python lib).

```
import SendKeys
SendKeys.SendKeys("{CAPSLOCK}")
```

## Linux

```
import fcntl
import os

KDSETLED = 0x4B32

console_fd = os.open('/dev/console', os.O_NOCTTY)

# Turn on caps lock
fcntl.ioctl(console_fd, KDSETLED, 0x04)

# Turn off caps lock
fcntl.ioctl(console_fd, KDSETLED, 0)
```

Edit xorg.conf

```
Section "InputDevice"
Identifier      "Generic Keyboard"
Driver          "kbd"
Option          "CoreKeyboard"
Option          "XkbRules"      "xorg"
Option          "XkbModel"      "pc104"
Option          "XkbLayout"     "us"
Option          "XkbOptions"    "ctrl:swapcaps"
EndSection
```

Use 'xmodmap' command.

```
xmodmap -e 'keycode 66 = Control_L'
xmodmap -e 'clear Lock'
xmodmap -e 'add Control = Control_L'
```

Edit .xmodemap file.
```
keycode 66 = Control_L
clear Lock
add Control = Control_L
```

## OS X

Keyboard Preference

