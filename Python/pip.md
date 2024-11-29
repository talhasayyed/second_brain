#pip #pipinstall 


### Stop pip from failing on single package when installing with requirements.txt
#pip #piperror 
[[pip]]

```
cat requirements.txt | xargs -n 1 pip install
```
[site](https://stackoverflow.com/questions/22250483/stop-pip-from-failing-on-single-package-when-installing-with-requirements-txt)


