[[Git]]

here n is your number for commit you want to squash

```
git rebase -i HEAD~n
```

then you will see open commit in vim 
something like 

```
pick hash
pisk hash
.
.
pick hash


```


change that to 
```
pick hash
s hash
s hash
.
.
s hash
```

```
git push -f origin mybranch:mybranch
```