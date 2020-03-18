

##### git use existing folder

	1- cd <localdir>
	2- git init
	3- git add .
	4- git commit -m 'message'
	5- git remote add origin http://tms.bmg.ng:7990/scm/mak/makeifly.git	( add new origin )
		OR
	6- git remote set-url origin https://github.com/anaircontec/makeifly.git ( change origin )

	7- git push -f origin master



##### To go back to a certain state of the project, use the git checkout command and provide the commit identifier.

	git log
	git checkout 4ea35ab9d43a8d6521bace280ae24477f799f132

	However, you actually don’t need to use the full length of identifier. Usually the first 5 characters are enough:

	git checkout 8d7e4e8


##### Git log

	git fetch origin
	git log origin/feature1  --oneline   ( log of remote branch )

	git config --global alias.lg "log --graph --abbrev-commit --decorate --pretty=format:'%C(red)%h%C(reset) - %C(cyan)%aD%C(reset)%C(green)(%ar)%C(reset)%n%''         %C(yellow)%d%C(reset)%C(white)%s%C(reset) %C(bold blue)<%an>%C(reset)' --all"

##### UnDo the changes
	how merge individual file from remote(github)

	git fetch origin
	git checkout origin/develop -- resources/views/booking/billing/pdfinvoice.blade.php ( get code From  develop branch of repo )
	git checkout resources/views/booking/billing/pdfinvoice.blade.php ( revert changes in locally )

	git checkout 3ef0d...














