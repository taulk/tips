# Win10 natural scrolling

Tested on Mac mini (late 2012) boot camp, wired mouse.

[Ref](http://tsentas.net/windows-bootcamp-reverse-scrolling/)

```
Open 'Control Panel'-'Mouse'-'Hardware'-'Properties'. # Get the device id.

Open 'regedit'.
Edit 'HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Enum\HID\VID_???\VID_???\Device Parameters' - 'FlipFlopWheel'.
Change value from '0' to '1'.
```
