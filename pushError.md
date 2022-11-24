Commands to pull request and merge for error in pushing

1. git fetch origin master:tmp

2. git rebase tmp

3. git push origin HEAD:master

4. git branch -D tmp
