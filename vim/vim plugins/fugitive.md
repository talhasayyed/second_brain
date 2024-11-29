## [[Git]]  [[vim]]


###### install fugitive to use git in vim 
```
mkdir -p ~/.vim/pack/tpope/start
cd ~/.vim/pack/tpope/start
git clone https://tpope.io/vim/fugitive.git
vim -u NONE -c "helptags fugitive/doc" -c q
```

keys 
`:G` to open fugitive window
`=` to unzip file 
`=` to zip it again
`-` to stage/unstage file (add)
`Enter` to move to file