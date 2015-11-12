# Shell

## Get shell script file path

[Ref](http://stackoverflow.com/questions/59895/can-a-bash-script-tell-what-directory-its-stored-in)

```
#!/bin/bash
DIR=$(dirname $0) # Bash(Ubuntu, OSX) tested.
DIR=$(dirname $(readlink -f $0))	# May be you need readlink. Not work on Bash(OSX).
```
