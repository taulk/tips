# OS X

## Must have
* [iterm2](http://www.iterm2.com)
* Xcode.
* Xcode command line tool. (xcode-select --install)
* [oh-my-zsh](http://ohmyz.sh)
* [homebrew](http://brew.sh) With tap.
* [Sublime Text](brew install Caskroom/cask/sublime-text.)
* [Vimari](https://github.com/guyht/vimari)

## Install Haskell ghci

```
brew install Caskroom/cask/haskell-platform
```

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


## Togle proxy

[Ref](https://stackoverflow.com/questions/4029471/how-to-you-toggle-on-and-off-a-web-proxy-in-os-x-from-the-command-line)

```
networksetup
networksetup -getsocksfirewallproxy wi-fi
networksetup -setsocksfirewallproxy wi-fi domain port
networksetup -setsocksfirewallproxystate wi-fi on
```

## Defaults

### Don't write .DS_Store to network stores. (Samba/FTP etc.)

```
defaults write com.apple.desktopservices DSDontWriteNetworkStores true
```

## PHP warning pgsql.so

[Ref](https://origin-discussions-us.apple.com/thread/7218739)
[Ref](http://stackoverflow.com/questions/6588174/enabling-postgresql-support-in-php-on-mac-os-x)

Solve by installing Server.app.

## URI encoding(%20 etc.) in filename

[rename](https://github.com/ap/rename)
[Ref](http://unix.stackexchange.com/questions/76500/how-to-remove-uri-encoding-from-file-names)
[Ref](http://unix.stackexchange.com/questions/174129/replace-20-with-a-space-in-filenames)
[Ref](http://unix.stackexchange.com/questions/159253/decoding-url-encoding-percent-encoding)

```
python -c "import sys, urllib as ul; print ul.unquote('$1');"
brew install rename
rename 'use URI::Escape; $_ = uri_unescape $_' filename
```

## Brew fast

```
cd /usr/local && git remote set-url origin my_url
brew update
```

## Show Library

Sol 0:

```
chflags nohidden ~/Library/
chflags hidden ~/Library/
```

Sol 1:
Magic 'Option'

## Disable safari from unzip downloaded file

Preference->General->Uncheck 'Open "safe" files'

## Open

```
man 1 open
open -a /Applications/TextEdit.app *.txt
open http://www.apple.com
ls | open -f
open -h NSView
open -a Xcode -h NSString.h
```

