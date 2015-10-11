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

