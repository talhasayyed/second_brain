#### [[Git]]

## git apply changes from text file or from clipboard

```
git diff > your_changes_name.txt
```

```
cp your_changes_name.txt /to/your/backup/dir
```

```
git apply your_changes_name.txt
```

## git remove/undo the applied changes from text file 
```
git apply --reverse your_changes_name.txt
```

