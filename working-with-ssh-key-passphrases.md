# [Solved]Working with SSH key passphrases
[Github](https://help.github.com/articles/working-with-ssh-key-passphrases/#platform-all)
[StackOverFlow](http://stackoverflow.com/questions/10032461/git-keeps-asking-me-for-my-ssh-key-passphrase)
## Solution:
```
eval $(ssh-agent)
ssh-add
```
