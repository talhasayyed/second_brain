
- ### vim modes

	- #### Enter command mode
	  - ==`Esc`== then ==`:`==
	  
	- #### Enter visual mode
		- ==`Esc`== then
		- ==`Ctrl`== + ==`v`==
		
	- #### Enter insert mode
		- ==`Esc`== then
		- ==`i`== or ==`Inset`==

----

#### *To move or jump to function / method in same file
move vim cursor to that word
==`Shift 8`== or  ==`*`==

#### vim delete all lines
enter command mode the
```
1,$d
```

#### Delete 

- #### delete single line
	enter command mode then
	`dd`

- #### delete multiple lines
	select by `Shift + v` then `↓` or `↑`  
	then delete by `dd`

----
### vim undo
`Esc` 
`u`

### vim redo
`Esc` 
`Ctrl + r`

----
### vim diff

- #### move in pane by
   `Ctrl + w`

- #### to copy content in vim diff from source to destination
	move to pane where content is present
	then `dp`
	
* #### to move content in vim diff
	move to pane where content is present
	then `do`

----

### vim folds

#### vim function level fold 
`z + m`

#### vim unfold all
`z + shift + r`



### Tab to space in vim
- `tabstop=4`: Sets the width of a tab character.
- `shiftwidth=4`: Sets the indentation width for auto-indent operations.
- `expandtab`: Converts tabs to spaces.
- `:retab`: Convert existing tabs to spaces in the file
