# Shell

## Get shell script file path

[Ref](http://stackoverflow.com/questions/59895/can-a-bash-script-tell-what-directory-its-stored-in)

```
#!/bin/bash
DIR=$(dirname $0) # Bash(Ubuntu, OSX) tested.
DIR=$(dirname $(readlink -f $0))	# May be you need readlink. Not work on Bash(OSX).
```

## Cat files

We have pat1, pat2, pat.. in different directories, we need to show content.

```
cat **/*pat*
find . -name 'pat' -exec cat {} \;
find . -name 'pat' -print | xargs cat
grep -R --include='**/*pat' '' *
```

## Default argument

[Ref](http://tldp.org/LDP/abs/html/parameter-substitution.html)

```
value=${1:-'default'}
```

## Curl

```
curl url
curl -d "key=value" url
curl -F "file=@filename;type=text/plain" url
curl -X GET url # GET, POST..
curl -I url # only care about header
curl -i url # also print response header
```

