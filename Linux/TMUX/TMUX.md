[[Terminals]]

[[TMUX Cheetsheet]]

```dataview
List 
from "Linux/TMUX"
```

### Reload tmux
```
tmux source-file ~/.tmux.conf
```
or set shortcut command from [[TMUX setup]] file

### Toggle
Toggle last active window
`CTRL + b l`

----

### Pane
create pane side wise 
`CTRL + b  %`

create pane up down (bottom)
`CTRL + b " `

kill pane 
`CTRL + b  x`


----
### Session
**show all sessions** `CTRL + b s`

#### move in sessions
##### move to previous session
`Ctrl + b (`
##### move to next session
`Ctrl + b )`

#### Detaching from Tmux Session
You can exit the Tmux session and return to your regular shell by typing:
`Ctrl + b` `d`

#### Re-attaching to Tmux Session
To attach to a session, you must first locate the session's name. Type the below command to receive a list of the currently active sessions.
##### list sessions
```bash
tmux ls
```

There are two Tmux sessions going, as you can see from the output. The first is referred to as `0` and the second is referred to as `my_named_session`.

For instance, to join the session `0`, you would type:
```bash
tmux attach-session -t 0
```

or attach tmux session by name
```
tmux attach-session -t my_session
```

#### Rename session
`Ctrl + b $`

----




