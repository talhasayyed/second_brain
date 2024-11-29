[[Terminals]]
[[zsh]]
#dotfiles 

```Bash
# Enable Powerlevel10k instant prompt. Should stay close to the top of ~/.zshrc.
# Initialization code that may require console input (password prompts, [y/n]
# confirmations, etc.) must go above this block; everything else may go below.
if [[ -r "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh" ]]; then
  source "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh"
fi

# If you come from bash you might have to change your $PATH.
# export PATH=$HOME/bin:/usr/local/bin:$PATH

# Path to your oh-my-zsh installation.
export ZSH="$HOME/.oh-my-zsh"
export GITHUB_TOKEN='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'

# Set name of the theme to load --- if set to "random", it will
# load a random theme each time oh-my-zsh is loaded, in which case,
# to know which specific one was loaded, run: echo $RANDOM_THEME
# See https://github.com/ohmyzsh/ohmyzsh/wiki/Themes


# ----------------------------------------------------------------
export OPENSSL_CONF=~/openssl.cnf

ZSH_THEME="robbyrussell"
# ZSH_THEME="powerlevel10k/powerlevel10k"

# typeset -g POWERLEVEL9K_INSTANT_PROMPT=quiet


# ----------------------------------------------------------------


# Set list of themes to pick from when loading at random
# Setting this variable when ZSH_THEME=random will cause zsh to load
# a theme from this variable instead of looking in $ZSH/themes/
# If set to an empty array, this variable will have no effect.
# ZSH_THEME_RANDOM_CANDIDATES=( "robbyrussell" "agnoster" )

# Uncomment the following line to use case-sensitive completion.
# CASE_SENSITIVE="true"

# Uncomment the following line to use hyphen-insensitive completion.
# Case-sensitive completion must be off. _ and - will be interchangeable.
# HYPHEN_INSENSITIVE="true"

# Uncomment one of the following lines to change the auto-update behavior
# zstyle ':omz:update' mode disabled  # disable automatic updates
# zstyle ':omz:update' mode auto      # update automatically without asking
# zstyle ':omz:update' mode reminder  # just remind me to update when it's time

# Uncomment the following line to change how often to auto-update (in days).
# zstyle ':omz:update' frequency 13

# Uncomment the following line if pasting URLs and other text is messed up.
# DISABLE_MAGIC_FUNCTIONS="true"

# Uncomment the following line to disable colors in ls.
# DISABLE_LS_COLORS="true"

# Uncomment the following line to disable auto-setting terminal title.
# DISABLE_AUTO_TITLE="true"

# Uncomment the following line to enable command auto-correction.
# ENABLE_CORRECTION="true"

# Uncomment the following line to display red dots whilst waiting for completion.
# You can also set it to another string to have that shown instead of the default red dots.
# e.g. COMPLETION_WAITING_DOTS="%F{yellow}waiting...%f"
# Caution: this setting can cause issues with multiline prompts in zsh < 5.7.1 (see #5765)
# COMPLETION_WAITING_DOTS="true"

# Uncomment the following line if you want to disable marking untracked files
# under VCS as dirty. This makes repository status check for large repositories
# much, much faster.
# DISABLE_UNTRACKED_FILES_DIRTY="true"

# Uncomment the following line if you want to change the command execution time
# stamp shown in the history command output.
# You can set one of the optional three formats:
# "mm/dd/yyyy"|"dd.mm.yyyy"|"yyyy-mm-dd"
# or set a custom format using the strftime function format specifications,
# see 'man strftime' for details.
# HIST_STAMPS="mm/dd/yyyy"

# Would you like to use another custom folder than $ZSH/custom?
# ZSH_CUSTOM=/path/to/new-custom-folder

# Which plugins would you like to load?
# Standard plugins can be found in $ZSH/plugins/
# Custom plugins may be added to $ZSH_CUSTOM/plugins/
# Example format: plugins=(rails git textmate ruby lighthouse)
# Add wisely, as too many plugins slow down shell startup.
plugins=(git)
plugins=(
	zsh-autosuggestions 
	# zsh-autocomplete 
	fast-syntax-highlighting
)

source $ZSH/oh-my-zsh.sh

# User configuration

# export MANPATH="/usr/local/man:$MANPATH"

# You may need to manually set your language environment
# export LANG=en_US.UTF-8

# Preferred editor for local and remote sessions
# if [[ -n $SSH_CONNECTION ]]; then
#   export EDITOR='vim'
# else
#   export EDITOR='mvim'
# fi

# Compilation flags
# export ARCHFLAGS="-arch x86_64"

# Set personal aliases, overriding those provided by oh-my-zsh libs,
# plugins, and themes. Aliases can be placed here, though oh-my-zsh
# users are encouraged to define aliases within the ZSH_CUSTOM folder.
# For a full list of active aliases, run `alias`.
#
# Example aliases
# alias zshconfig="mate ~/.zshrc"
# alias ohmyzsh="mate ~/.oh-my-zsh"

# To customize prompt, run `p10k configure` or edit ~/.p10k.zsh.
[[ ! -f ~/.p10k.zsh ]] || source ~/.p10k.zsh


export OPENSSL_CONF=~/openssl.cnf

# export PYENV_ROOT="$HOME/.pyenv"
# command -v pyenv >/dev/null || export PATH="$PYENV_ROOT/bin:$PATH"
# eval "$(pyenv init -)"
# eval "$(pyenv virtualenv-init -)"

export PATH="$HOME/.pyenv/bin:$PATH"
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"

export LD_LIBRARY_PATH=$HOME/instantclient_21_3:$LD_LIBRARY_PATH

alias grepc='grep --color=always'

alias cc="clear"
alias reload="exec zsh -l"
alias update="source ~/update_linux.sh"
alias update_obsidian="source ~/update_obsidian.sh"

alias work='~/work'
alias obs="~/Obsidian\ vault"

# proj alias
alias act="~/work/acceptancechecklist"
alias fmcm="~/work/fmcm"
alias vcmkr="~/work/vcmkr"
alias standalonecm="~/work/vcmkr"
alias goc="~/work/goc_disconnect"

# User specific aliases and functions
alias mps="ps aux | grep 'python' | grep 'opst'"
alias pipp="pip --proxy 'dcoeng1-cob-dev.tnc.virtela.cc:3128'"
alias llp='ls -l --color=auto *.py'
alias llr='ls -lhtr'
alias llt='ls -lhtr | tail'
export GIT_SSH='/opt/opst/shared_git.sh'
export GIT_AUTHOR_NAME=$(logname)
export GIT_AUTHOR_EMAIL=${GIT_AUTHOR_NAME}@nttglobal.net

# Alias 
alias g='git '
alias gs='git status'
alias gsm='git status | grep modified:'
alias ga='git add'
alias gst='git status '
alias gd='git diff '
alias grv='git remote -v '
alias gb="git branch"
alias gc="git checkout"
alias ggraph="git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --all --color"
#alias gg="git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --all --color"
#alias gg="git log --graph --pretty=format:'%Cred%h%Creset -%C(bold yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --all --color"
#alias gg5='gg | head -n 5'
#alias gg10='gg | head -n 10'
alias gfa='git fetch --all'
alias gph_m='git push origin master:master'
alias gpu_m='git pull origin master:master'
alias gph_d='git push origin develop:develop'
alias gpu_d='git pull origin develop:develop'
alias gdiff='git difftool'


alias ll='ls -lhtr'
alias o='less '  
alias updateobsidian="source ~/update_obsidian.sh"

# git stash alias
alias gsd0="git stash drop stash@{0}"
alias gst="git stash"
alias gps="git pop stash"
alias gstap0="git stash apply stash@{0}"
alias gstuat="git stash apply stash^{/'uat-settings'}"
alias gstrm="git stash && git stash drop stash@{0}"
alias gstls="git stash list"
#

alias py="python"
alias sshlist="cat vim ~/.ssh/config"
alias prac="~/work/code_rev"

export EDITOR=vim

# gg 5 alias
gg() {
    local lines=${1:-}  # Default to no limit if no argument is given
    if [[ -n $lines ]]; then
        git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --all --color | head -n "$lines"
    else
        git log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --all --color
    fi
}



ORACLE_HOME=/usr/lib/oracle/12.2/client64/ 
PATH=$PATH:$ORACLE_HOME/bin 
LD_LIBRARY_PATH=$ORACLE_HOME/lib:$LD_LIBRARY_PATH 


# tsayyed
# Add this function to your .bashrc
mvim() {
    # Split the input argument into filename and line number
    local input="$1"
    local filename=$(echo "$input" | cut -d ':' -f 1)
    local linenumber=$(echo "$input" | cut -d ':' -f 2)
    # Construct the vim command
    vim +$linenumber $filename                                                                                                                                                                                                              
}

# fzf setup
# Set up fzf key bindings and fuzzy completion


```