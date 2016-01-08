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

## Change commit time

[Ref](http://stackoverflow.com/questions/454734/how-can-one-change-the-timestamp-of-an-old-commit-in-git)

```
git commit --amend --date="Wed Feb 16 14:00 2011 +0100"
```
