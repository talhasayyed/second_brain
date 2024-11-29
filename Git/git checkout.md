#### [[Git]]

git checkout only particular file from branch
```
git checkout <branch_name> -- <file_path>
```




#### if you are already on some branch b1 you made changes, now you want create on another branch b2 apply files from branch B1

`git checkout b1`
`git status b1`
output: 
file1
file2
file3

now if you just want file2 and file3 in b2 branch then

`git checkout b1`
create new branch
`git checkout -b b2`
`git add file2 file3`
`git commit -m "msg"`
`git push origing b2`
