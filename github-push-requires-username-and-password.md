#[Solved]Github push require username and password

[StackOverFlow](http://stackoverflow.com/questions/6565357/git-push-requires-username-and-password)

## Solution:
Use the ssh url.
```
git remote set-url origin git@github.com:username/repo.git
```
## Update:
Use the ssh url to clone at the very first.
```
git clone git@github.com:username/repo.git
```
