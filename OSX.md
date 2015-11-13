# OS X

## Must have
* [iterm2](http://www.iterm2.com)
* Xcode.
* Xcode command line tool. (xcode-select --install)
* [oh-my-zsh](http://ohmyz.sh)
* [homebrew](http://brew.sh) With tap.
* [Sublime Text](brew install Caskroom/cask/sublime-text.)
* [Vimari](https://github.com/guyht/vimari)

## System Preference

Keyboard -> Shortcuts -> All controls(^F7)


## Display the Full Path in Mac Finder Window Titlebars
[Ref](http://osxdaily.com/2007/12/02/show-full-directory-path-in-finder-window-title-bars/)
Tested on OS X El Capitan
```
defaults write com.apple.finder _FXShowPosixPathInTitle -bool YES
killall Finder
```

## Build-in Apache & PHP

in /etc/apache2/httpd.conf uncomment:

```
LoadModule php5_module libexec/apache2/libphp5.so
```

to enable php, restart Apache.

```
apachectl restart
```

update the 'DocumentRoot'.



