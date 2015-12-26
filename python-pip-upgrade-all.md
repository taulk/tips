# pip upgrade all

[Github issue](https://github.com/pypa/pip/issues/59)
[Ref](http://mikegrouchy.com/blog/2014/06/pro-tip-pip-upgrade-all-python-packages.html)

```
sudo pip freeze --local | grep -v '^\-e' | cut -d = -f 1  | xargs sudo pip install -U
```
