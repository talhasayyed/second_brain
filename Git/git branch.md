### [[Git]]

### to delete local branch
To delete a local branch that has been fully merged, you can use `git branch -d`:

Click to Copy
```
git branch -d branch-to-delete
```


To delete a local branch that has not been fully merged (i.e. force delete), you must use `git branch -D`:

Click to Copy

```
git branch -D branch-to-delete
```


### to delete remote branch
```
git push <remote_name> --delete <branch_name>
```
