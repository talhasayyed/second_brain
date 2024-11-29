
#dotfiles

```
#unbind C-b  
#set -g prefix C-a  
#bind-key C-a last-window  
#set-window-option -g mode-keys vi  
#  
#  
## use vim-like keys for splits and windows  
#bind-key v split-window -h -c "#{pane_current_path}"  
#bind-key s split-window -v -c "#{pane_current_path}"  
#bind-key h select-pane -L  
#bind-key j select-pane -D  
#bind-key k select-pane -U  
#bind-key l select-pane -R  
#  
  
set -g default-terminal "screen-256color"  
set -ga terminal-overrides ",*256col*:Tc"  
  
set -g mouse on
```