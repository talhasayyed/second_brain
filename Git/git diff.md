[[Git]]
to get diff of all files 
```
git diff
```


to get diff of specific file
```
git diff file.txt
```


to get diff filename only
```
git diff --name-only
```


to get diff between 2 hashs
```
git diff hash1..hast2
```


git diff between 2 files 
```
git diff --no-index file1.txt file2.txt
```


git diff after commmit before push
```
git show
```


alternatively if `git reset soft~1` and git diff is not showing 
then it is in cached area try
```
git diff --cached
```

to remove changes from cached area 
```
git reset
```