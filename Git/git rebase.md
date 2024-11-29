### [[Git]]

```
git add --all
git commit -m "msg"
git rebase -i master <branch_name>
```

	if conflicts in rebase the resolve conflict
		go to file and resolve (grep -irn <<<<)
		choose the part you want to keep,
	else
		*rebase Successfully*
		
```
git push origin master
```

or 

```
git checkout feature  
git rebase master // use with -i option for interactive
```



![git rebase gif](https://miro.medium.com/v2/resize:fit:720/format:webp/0*JRt9VF_osaAoVwKg.gif)


[rebase details](https://nvie.com/posts/a-successful-git-branching-model/?source=post_page-----d8b91825bbb1--------------------------------)
