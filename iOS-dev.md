# iOS Dev

## Remove Xcode Simulator

[Ref](http://www.wugaojun.com/blog/2015/08/23/tong-guo-ming-ling-xing-kuai-su-shan-chu-xcodemo-ni-qi/)

```
xcrun simctl list
xcrun simctl delete {UUID}
xcrun simctl erase {UUID}
xcrun simctl erase all
```
