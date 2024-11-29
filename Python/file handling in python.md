[[Python]]

#### Read json file to dict (using with)
```Python
import json
with open('file.json', 'r') as f:
    dict_value = json.load(f)
print(dict_value)
```


#### Write file in python (using with)
```Python
with open('myvar.txt', 'a') as file: 
	file.write(str(myvar) + '\n')
```

