
### [[Git]]


one line log
```
git log --oneline
```

git last n log in one line
```
git log -n 2 --oneline
```



git last n log of particular user
```
git log -n 2 --author=<username>
```



#### To show Git Graph
```
git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --all
```
:Q
