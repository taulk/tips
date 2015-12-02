# Chrome

## Get memory usage

[Ref](http://zhuanlan.zhihu.com/iobject/19845233)

chrome://memory

```
top -l 1 -stats mem,command | grep Chrome | cut -d' ' -f1 | awk '/K/ { gsub(/K.*$/,""); sum+=$1} /M/ { gsub(/M.*$/,""); sum+=$1*1024} END {printf "%.2fM\n", sum/1024} '
```
