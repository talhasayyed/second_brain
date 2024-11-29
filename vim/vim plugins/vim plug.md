[[vim]]
vim plug is plugin manager for vim
### Install vim plug in linux 
```
curl -k -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```



### install plugin using vim plug
eg:
add this  lines to `~/.vimrc` file (==mandatory==)
```
call plug#begin('~/.vim/plugged')  
" Plug 'plugin-author/plugin-name'   " Add plugin lines here  
call plug#end()
```


