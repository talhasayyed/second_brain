[[Python]]

### Facing difficulty while install pyenv on Linux 

Solution : on Linux home directory open terminal 
```
sudo apt-get install -y make build-essential libssl-dev zlib1g-dev \  libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev \  libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl 
```


```
curl https://pyenv.run | bash   
```

or 
```
curl -L https://github.com/pyenv/pyenv-installer/raw/master/bin/pyenv-installer | bash 
```

in vim ~/.bashrc
```
export PATH="/home/user/.pyenv/bin:$PATH"  
eval "$(pyenv init -)"  
eval "$(pyenv virtualenv-init -)" 
```

terminal
```
pyenv --help
```

After installation check the version 
```
pyenv install --list | grep 3.7. 
3.7.0  
3.7.1
```


## pyenv virtualenv steps

https://realpython.com/intro-to-pyenv/

#### remove / delete pyenv env_name
```
pyenv uninstall your_venv
```