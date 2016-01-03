# loop

[Ref](http://tldp.org/LDP/abs/html/loops1.html)
[Example](http://www.thegeekstuff.com/2011/07/bash-for-loop-examples/)
[SO](http://stackoverflow.com/questions/8645546/for-name-in-ls-and-filenames-with-spaces)

## Handle space in filename

example:

```
for name in *; do echo $name; done	# instead of in `ls`
ls | while read name; do echo $name; done
```
