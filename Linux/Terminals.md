#linux #terminal

[[Linux]] [[Terminals]]
### [[linux tools]]


[ZSH Terminal](https://ohmyz.sh/)
Usefull wile using git etc.

#### restart terminal
for bash terminal `exec -l bash`
for zsh terminal `exec -l zsh`
#### reload terminal
for bash terminal `source ~/.bashrc`
for zsh terminal `source ~/.bashrc`

[[TMUX]]

----
## ls

ls additional info
```bash
ls -lhrt
```

## ls only folder
```bash
ls -d */
```


#### ls exclude file type
```bash
ls -I "*.log"
```
or 
```bash
ls --ignore="*.log"
```


#### ls exclude multiple file type
```bash
ls -I "*.log" -I "*.csv"
```
or 
```bash
ls --ignore="*.log" --ignore="*csv"
```
or 
```bash
ls --ignore={"*.jpg","*.png","*.svg"}
```

