#### alias should be added in `~/.bashrc` or `~/.zshrc` based on what terminal you are using


## git alias

```
alias gb="git branch --color | grep '*'"
alias gba="git branch"
alisa gc="git checkout"
alias gsm="git status --color | grep 'modified:'"

alias gfa="git fetch --all"
alias gph="git push origin"
alias gpl="git pull origin"
```

```
# git stash alias  
alias gsd0="git stash drop stash@{0}"  
alias gst="git stash"  
alias gps="git pop stash"    
alias gstap0="git stash apply stash@{0}"  
alias gstuat="git stash apply stash^{/'uat-settings'}"  
alias gstrm="git stash && git stash drop stash@{0}"  
alias gstls="git stash list"  
#
```


incase to unset or remove alias incase alias error
```
unalias gg 2>/dev/null\n
```

#### gg
```
alias gg="git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --all --color"
```
or
dynamic gg 
eg :- `gg 5` for 5 line
```
# gg 5 alias
gg() {
    local lines=${1:-}  # Default to no limit if no argument is given
    if [[ -n $lines ]]; then
        git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --all --color | head -n "$lines"
    else
        git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --all --color
    fi  
}
```