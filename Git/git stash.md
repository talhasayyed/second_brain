#### [[Git]]

#### create stash
```
git stash
```
#### create stash by stash name
```
git stash save "stash_name"
```


to get list of stash 
```
git stash list
```

git stash drop at 0 index
```
git stash drop stash@{0}
```

git stash pop will apply and remove stash from stash list
```
git pop stash
```


### git stash show
show stash of 0 index
```
git stash show stash@{0}
```

#### Apply stash

to apply stash to git by index number
eg: apply stash of index 0
```
git stash apply stash@{0}
```

To apply stash by stash name
```
git stash apply stash^{/'uat-settings'}
```

----

#### undo local changes and remove changes from branch

it will  create new stash and move the changes on that stash which will be on index 0
and drop stash of index 0
```
git stash && git stash drop stash@{0}
```

----



stash [[alias]] are also there

### Stash untracked file
```
git stash --include-untracked
```