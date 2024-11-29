#### [[Git]]

To merge your feature branch (`Mybranch`) into your main branch (`master`), you'll typically follow these steps:

**Checkout the Main Branch**: First, switch to your main branch.
`git checkout master`
`git pull origin master`
`git merge Mybranch`
`git commit -m "Merge Mybranch into master"`

if merge conflict (do not push) 
	if conflict
	`git merge --abort`
	`git checkout <branch_name>`
	`git rebase -i master <branch_name>`
		if conflicts in rebase the resolve conflict
			go to file and resolve (grep -irn <<<<)
			choose the part you want to keep,
		else
			*rebase Successfully*
	then 
	`git commit -m "msg"`
else
`git push origin master`



![git merge --no-ff vs git merge](https://miro.medium.com/v2/resize:fit:720/format:webp/0*6OWQ6E6bT-TmuEvJ.png)
