[[Python debugging]]
### to add debugger line pdb

`import pdb; pdb.set_trace()`

#### when in break point line
(pdb) 

`n` for continue to next line

`c` for continue

`l` for show on which line you are in code


##### to paste variable value in file while in pdb
with open single liner / (1) one line 
eg:- myvar is variable
```
with open('myvar.txt', 'a') as file: file.write(str(myvar) + '\n')
```



### tool
```
pip install pdbp
```

```
pip install ipdb
```

```
pip install pdbpp
```
to see code type `sticky`
