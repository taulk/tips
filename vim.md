# VIM

## Save as sudoer
[vim wikia](http://vim.wikia.com/wiki/Su-write)
```
:w !sudo tee % > /dev/null
:%!sudo bash -c "cat > '%'"
```
Or make a command so :W invokes sudo:
```
command W w !sudo tee % > /dev/null
```

## neocomplete lua for spf13

[Ref](https://github.com/spf13/spf13-vim/issues/773)

install vim-nox

## remove self

```
:call delete(expand('%'))
```
