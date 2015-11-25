# Git

## Removing a remote tag

[Ref](http://stackoverflow.com/questions/5480258/how-to-delete-a-remote-git-tag)

```
git push origin :tagname
```

## Show remote and local head diff

```
git fetch
git log origin/master..master
```

