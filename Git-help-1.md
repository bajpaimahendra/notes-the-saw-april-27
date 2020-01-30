https://guides.github.com/activities/hello-world/
https://www.youtube.com/watch?v=FyAAIHHClqI
https://www.youtube.com/watch?v=UuHxzM9r-0M

##### Install Git
	
	sudo apt-get install git	( Install )
	git --version			( check version )
	git config --list		( check configuration )

##### Customize Git Environment

	git config --global user.name "Mahendra"
	git config --global user.email "mahendra.bajpai@cg-infotech.com"
	git config --global branch.autosetuprebase always	           ( Avoid merge commits for pulling )
	git config --global color.ui true				   ( Color highlighting )
	git config --global color.status auto				   ( Color highlighting )
	git config --global color.branch auto				   ( Color highlighting )
	git config core.fileMode false					   ( inside project dir after clone)

##### git use existing folder

	1- cd <localdir>
	2- git init
	3- git add .
	4- git commit -m 'message'
	5- git remote add origin http://tms.bmg.ng:7990/scm/mak/makeifly.git	( add new origin )
		OR
	6- git remote set-url origin https://github.com/anaircontec/makeifly.git ( change origin )

	7- git push -f origin master

##### .gitignore is now working


	git rm -r --cached .	( rm all files )
	git add .		( add all files as per new .gitignore )
	git commit -m ".gitignore is now working" ( now, commit for new .gitignore to apply)


##### Show Current  Branch In Terminal	

	paste below code at the end of file /home/bajpai/.bashrc
		
	parse_git_branch() {
	  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
	}

	#export PS1="\u@\h \[\033[33m\]\$(parse_git_branch)\[\033[00m\] ${debian_chroot:+($debian_chroot)}\w $ "

	#export PS1="\u@\h \[\033[32m\]\w\[\033[33m\]\$(parse_git_branch)\[\033[00m\] $ "

	#export PS1="\u@\h \[\033[32m\]\w\[\033[33m\]\$(parse_git_branch)\[\033[00m\] $ "


	PS1='\[\033[0;32m\]\[\033[0m\033[0;32m\]\u\[\033[0;36m\] @ \[\033[0;36m\]\h : \w\[\033[0;32m\]$(__git_ps1)\n\[\033[0;32m\]└─\[\033[0m\033[0;32m\]▶ \$ \[\033[0m\]'


##### diffmerge settings

		
	git config --global diff.tool diffmerge
	git config --global difftool.diffmerge.cmd "/usr/bin/diffmerge \"\$LOCAL\" \"\$REMOTE\""
	git config --global mergetool.keepBackup false
	git config --global merge.tool diffmerge
	git config --global mergetool.diffmerge.trustExitCode true
	git config --global mergetool.diffmerge.cmd "/usr/bin/diffmerge --merge --result=\"\$MERGED\" \"\$LOCAL\" \"\$BASE\" \"\$REMOTE\""


##### Track newly create remote branch

	git fetch --all
	git branch --track branch-name origin/branch-name


##### Change origin

	git remote set-url origin https://mahendravrn@bitbucket.org/visitatvishal82/tawarmall.git


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
	how merge individual file from remote

	git fetch origin
	git checkout origin/develop -- resources/views/booking/billing/pdfinvoice.blade.php ( get code From  develop branch of repo )
	git checkout resources/views/booking/billing/pdfinvoice.blade.php ( revert changes in locally )

	git checkout 3ef0d...














