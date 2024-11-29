
[[Git]]
[[git stash]]


#### Create Patch file in git
```bash
# Apply the uat-settings stash
git stash apply stash@{2}

# Temporarily commit the changes
git add .
git commit -m "Temporary commit for uat-settings stash"

# Create the patch file
git format-patch -1 HEAD

# Revert the temporary commit
git reset HEAD~1

```

```bash
git checkout -- .
```


### Applying a Patch with `git apply`
```bash
git apply 0001-Temporary-commit-for-uat-settings-stash.patch
```
eg:-
```bash
# Navigate to the repository
cd /path/to/your/repository

# Apply the patch
git apply 0001-Temporary-commit-for-uat-settings-stash.patch

# Check the changes
git status
git diff

# Commit the changes
git add .
git commit -m "Apply patch for uat-settings stash"

```

### Applying a Patch with `git am`

`git am` is used to apply the patch and automatically create a commit.

**Navigate to your repository directory**:
```bash
cd /path/to/your/repository
```

**Apply the patch and create a commit**:
```bash
git am <patch-file>
```

For example, if your patch file is named `0001-Temporary-commit-for-uat-settings-stash.patch`:
```bash
git am 0001-Temporary-commit-for-uat-settings-stash.patch
```


### Handling Conflicts

If there are conflicts when applying the patch, Git will pause and prompt you to resolve them.

1. **Resolve conflicts**: Manually edit the conflicting files to resolve the conflicts.    
2. **Mark conflicts as resolved**:
	```git add <resolved-files>```
3. **Continue applying the patch**:
	```git am --continue```
4. **Abort applying the patch** (if you want to cancel the patch application): 
	```git am --abort```

eg:- using am
```bash
# Navigate to the repository
cd /path/to/your/repository

# Apply the patch and create a commit
git am 0001-Temporary-commit-for-uat-settings-stash.patch
```


### git apply 
git apply 
paste 
then `ctrl + d`