#### [[TMUX]]

add this lines to `~/.tmux.conf` file
```
# set mouse click on
set -g mouse on

# reload shortcut for tmux
bind r source-file ~/.tmux.conf

# vim theme color on tmux
set -g default-terminal "screen-256color"
set -g default-terminal "screen-256color"
set -ga terminal-overrides ",*256col*:Tc"
```