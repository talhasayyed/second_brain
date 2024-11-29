#Linux 
[[server]]
#### server side usefull
```dataview
List 
from "Linux/server side usefull"
```
#### TMUX
```dataview
List 
from "Linux/TMUX"
```


#### find path of any linux app
```which appname```


[[grep]] #grep
#### Find string in filepath recursive
```grep -rnw /path/ -e 'pattern' ```


#ssh
## Connect to server ssh
```bash
ssh username@servername
```


## Connect NTT server ssh
```bash
ssh username@servername.tnc.virtela.cc
```


## Copy from server to pc
```
scp username@serverurl:/path pcpath
```
<Br><Br>
## Copy file from NTT server

#### 1. Change user to opst
```bash
sudo -iu opst
```
##### Now server name is 
#NTT
```
opst@servername.tnc.virtela.cc
```
#### 2. Move file to temp /tmp folder
* Change permission 
```bash
chmod ugo+rwx filename 
```
* find and check permission changed
```bash
la -l | grep filename
```


#### Find last created files
- To just find file created 10min ago
```bash
find . -maxdepth 1 -type f -mmin -10
```
- To find and delete file created 10min ago
```bash
find . -maxdepth 1 -type f -mmin -10 -exec rm {} \;
```


#### Move file
```mv [option] sourcepath destinationpath```

#### Remove folder in Linux
```rm [option] foldername```
```bash
rm -vrf foldername
```


#### To check the process in Linux
```ps aux```
```ps aux | grep yourprocessname```


#### Find command history in Linux
```ctrl + r```


#### SCC calculate the price of the code




#### Find Process in Linux 
```bash
ps -p
```
Then tab and find process name and select 
It will select process id of it



##### show pretty json in terminal
```bash
cat myfile.json | python -m json.tool
```


#### show process in linux
```bash
ps awx
```
#### find process folder path from process id
```
pwdx <PID>
```
##### show python process in linux
```bash
ps awx | grep python
```
##### show python process that have foldername
```bash
ps awx | grep python | grep foldername
```

#### kill process in linux
```bash
kill <PID>
```
##### kill process by foldername
```bash
pkill -f foldername
```


