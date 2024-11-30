#linux #terminal

[[Linux]] [[linux command]]
### [[linux tools]]


[ZSH Terminal](https://ohmyz.sh/)
Usefull wile using git etc.



[[tmux]]

----
## ls

ls additional info
```bash
ls -lhrt
```

## ls only folder directory
```bash
ls -d */
```


#### ls exclude file type
```bash
ls -I "*.log"
```
or 
```bash
ls --ignore="*.log"
```


#### ls exclude multiple file type
```bash
ls -I "*.log" -I "*.csv"
```
or 
```bash
ls --ignore="*.log" --ignore="*csv"
```
or 
```bash
ls --ignore={"*.jpg","*.png","*.svg"}
```


#### To check multiple installed packages in linux
eg:-
```bash
dpkg -l |egrep 'python-dev|libsasl2-dev|libssl-dev|libldap2-dev'
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


#### find which app is running on perticualr port number
-p for port
```bash
netstat -anopl | grep <portnumber>
```
take the port value and 

```bash
pwdx  46669
```


#### find process by port number and kill
```bash
netstat -anopl | grep <portnumber> | awk "{print \$7}" | cut -d "/" -f1 | xargs kill
```


#### split in line in linux to find word
select word from line linux
eg:-
`tcp        0      0 0.0.0.0:9001            0.0.0.0:*               LISTEN      1982320/python       off (0.00/0/0)`

```
<command> | awk "{print \$7}"
```
output
`1982320/python`


#### split by charater in linux
cut in commands
eg:-
`1982320/python`
```
<command> | cut -d "/" -f1
```
output 
`1982320`



### Create symlink
virtual box shared folder
mount `vboxsf SharedVMFolder` to  `/media/sf_SharedVMFolder`

**Ensure the shared folder is properly mounted**: First, make sure that your shared folder is successfully mounted at `/media/sf_SharedVMFolder/`. If the folder isn’t already mounted, run:
```
sudo mount -t vboxsf SharedVMFolder /media/sf_SharedVMFolder
```

**Create the target folder**: If `/home/tsayyed/sharedVMFolder/` does not already exist, you can create it by running:
```
mkdir -p /home/tsayyed/sharedVMFolder
```

**Create the symlink**: Now, create a symbolic link from `/home/tsayyed/sharedVMFolder/` to `/media/sf_SharedVMFolder/`:
```
ln -s /media/sf_SharedVMFolder /home/tsayyed/sharedVMFolder
```
This command creates a symlink (`ln -s`) where `/home/tsayyed/sharedVMFolder/` will appear as if it’s directly accessing `/media/sf_SharedVMFolder/`. Any changes in `/media/sf_SharedVMFolder/` will automatically reflect in `/home/tsayyed/sharedVMFolder/` and vice versa.

**Verify the Symlink**: You can verify that the symlink was created correctly by checking it:
```
ls -l /home/tsayyed/sharedVMFolder
```
**Access the Folder**: Now, you can access your shared folder through `/home/tsayyed/sharedVMFolder/`, and any file changes will automatically be reflected in `/media/sf_SharedVMFolder/`.

**NOTE:**
**Permissions**: Sometimes, the default mount of shared folders in VirtualBox may require additional permissions. If you encounter issues with access (e.g., "permission denied"), you might need to add your user to the `vboxsf` group, which is the group used by VirtualBox to manage shared folders:
```
sudo usermod -aG vboxsf $USER
```
After this, log out and log back in, and you should have the necessary permissions to access the shared folder without issues.

### live log details, tail log
```
tail -f logfile.log
```