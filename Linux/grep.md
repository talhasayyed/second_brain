
#importpdb #grep
to find only import pdb whitout # in start in python file
```
grep -irn "^[^#]*import pdb; pdb.set_trace()" --include="*.py"
```


##### grep exclude file
```bash
grep -r --exclude='*.txt' pattern .
````


##### grep exclude word
```bash
grep -v 'Paul'
```

#### grep 2 line above
```bash
grep -A 2 foo README.txt
```
#### grep 2 line below
```bash
grep -B 2 foo README.txt
```
#### grep 2 line below and above
```bash
grep -C 2 foo README.txt
```


### Excluding Multiple Patterns

You might be wondering, ‘Can I exclude more than one pattern at a time?’ Absolutely! To do this, you simply use the ‘-v’ option with the ‘-e’ option for each pattern you want to exclude.

For instance, 
```bash
grep -v -e 'pattern1' -e 'pattern2' filename
```
will exclude both ‘pattern1’ and ‘pattern2’ from your search results



### Using Regular Expressions

Let’s venture into the world of regular expressions, or regex. Regex is a sequence of characters that define a search pattern. When used with grep, they can provide a new level of control over your pattern exclusion.

For example, you can use a regex to exclude all lines that start with a specific word. The command `grep -v '^word' filename` will exclude all lines starting with ‘word’. The ‘^’ symbol is a regex that matches the start of a line.

```bash
grep -v '^word' filename
```

