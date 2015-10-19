# OS X

## Display the Full Path in Mac Finder Window Titlebars
[Ref](http://osxdaily.com/2007/12/02/show-full-directory-path-in-finder-window-title-bars/)
Tested on OS X El Capitan
```
defaults write com.apple.finder _FXShowPosixPathInTitle -bool YES
killall Finder
```
