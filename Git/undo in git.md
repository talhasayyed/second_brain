#### [[Git]]

#git #gitundo #gitreset


[Example](https://www.gitkraken.com/learn/git/git-reset#:~:text=The%20first%20of%20the%20three,the%20changes%20in%20the%20index)


![git reset image](https://www.howtogeek.com/wp-content/uploads/csit/2021/07/f5026f58.png?trim=1,1&bg-color=000&pad=1,1)


git reset --soft HEAD~|500



### [[git reset]]

```
git reset --hard 2
```

```
git reset --hard HEAD
```

![git reset gif](https://joshua-laughner.io/static/posts/img/git-tutorial-pt1/4-reset.gif)





undo local commit before push
```
git reset HEAD~1
```



if want to remove all local changes 
last resort
##### [[Delete .git folder and restart again]]



remove file from git
```
git rm <file>
```

```
git commit -m "your commit"
```

```
git push origin <branch name>
```



