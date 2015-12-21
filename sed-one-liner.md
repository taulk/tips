# Sed one liner

Inspired by [Sed-One-Liner](http://www.catonmat.net/series/sed-one-liners-explained)

## Reverse order of lines

Like 'tac' in *nix-like os.

```
sed '1!G;h;$!d'
```
