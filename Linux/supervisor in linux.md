

#### Supervisor env
```
.local/bin/supervisorctl
```
or
```
source super_venv/bin/activate
```



to run app on supervisor / auto start
`cd`

```
cd ~/supervisor/configs
```

create supervisor app
```
[program:<app_name>]             
directory=<app_dir>                          
command=<venv_python_path> -u <file.py>                                                                          
autostart=true                                
autorestart=true
stderr_logfile=<output_file_path>.out.log 
stdout_logfile=<output_file_path>.out.log
```



#### Start supervisor app
```
update
```
and
```
start appname
```
reload [[NGNIX]]

##### to check list of all app in supervisor 
```
status
```

#### restart supervisor app
```
restart appname
```
#### stop supervisor app
```
stop appname
```
