[[vim]]
#dotfiles
```
set backspace=2
set hlsearch
set showcmd
set showmatch
set ignorecase
set smartcase
set incsearch
set autowrite
set hidden
set nu
set mouse=a
set et
set tabstop=4
set sw=4
set nofoldenable
set foldmethod=indent 
set termguicolors
set cursorline
set paste
" Ensure Vim saves files with Unix line endings (LF)
set fileformats=unix,dos
set fileformat=unix


"set foldmethod=syntax  " or use 'indent' for indentation-based folding
"set foldlevel=1        " Initially collapse all folds


:high clear CursorLine  gui=underline cterm=underline
au InsertEnter * set cul
au InsertLeave * set nocul

call plug#begin('~/.vim/plugged')
" Gruvbox theme
Plug 'morhetz/gruvbox'


Plug 'tpope/vim-surround'

"" Track the engine.
Plug 'SirVer/ultisnips'
"" Snippets are separated from the engine. Add this if you want them:
Plug 'honza/vim-snippets'

" gitgutter
"Plug 'airblade/vim-gitgutter'
" minimap
call plug#end()

" Enable filetype detection, plugins, and indentation
filetype plugin indent on
syntax enable

let g:UltiSnipsSnippetDirectories=["UltiSnips"]

" Use Tab for snippet expansion (if using UltiSnips)
imap <silent><expr> <tab> pumvisible() ? "\<C-n>" : "\<Tab>"
smap <silent><expr> <tab> pumvisible() ? "\<C-n>" : "\<Tab>"

"" Track the engine.
"Plug 'SirVer/ultisnips'
"
"" Snippets are separated from the engine. Add this if you want them:
"Plug 'honza/vim-snippets'
"
"" Trigger configuration. Do not use <tab> if you use https://github.com/Valloric/YouCompleteMe.
"let g:UltiSnipsExpandTrigger="<tab>"
"let g:UltiSnipsJumpForwardTrigger="<tab>"

" Use UltiSnips for snippets
let g:UltiSnipsExpandTrigger = '<tab>'
let g:UltiSnipsJumpForwardTrigger = '<c-j>'
let g:UltiSnipsJumpBackwardTrigger = '<c-k>'
" Filetype-specific snippets
let g:UltiSnipsSnippetDirectories=['UltiSnips']

"source ~/fzf_file.sh

""""" for 'jacoborus/tender.vim' theme
"call plug#begin('~/.vim/plugged')
"Plug 'jacoborus/tender.vim'
"call plug#end()
"
"" If you have vim >=8.0 or Neovim >= 0.1.5
"if (has("termguicolors"))
" set termguicolors
"endif
"" For Neovim 0.1.3 and 0.1.4
"let $NVIM_TUI_ENABLE_TRUE_COLOR=1
"" Theme
"syntax enable
""colorscheme tender

"""" for 'artanikin/vim-synthwave84'
"call plug#begin('~/.vim/plugged')
"Plug 'artanikin/vim-synthwave84'
"call plug#end()
"if (has("termguicolors"))
" set termguicolors
"endif
"colorscheme synthwave84
"


"Plug 'ayu-theme/ayu-vim' " or other package manager
""...
"set termguicolors     " enable true colors support
""let ayucolor="light"  " for light version of theme
""let ayucolor="mirage" " for mirage version of theme
"let ayucolor="dark"   " for dark version of theme
"colorscheme ayu

Plug 'junegunn/fzf', { 'do': { -> fzf#install() } }
Plug 'junegunn/fzf.vim'

colo gruvbox

```