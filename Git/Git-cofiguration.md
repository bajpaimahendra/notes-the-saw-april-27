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


##### Show Current  Branch In Terminal	

	paste below code at the end of file /home/bajpai/.bashrc
		
	parse_git_branch() {
	  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
	}

	#export PS1="\u@\h \[\033[33m\]\$(parse_git_branch)\[\033[00m\] ${debian_chroot:+($debian_chroot)}\w $ "

	#export PS1="\u@\h \[\033[32m\]\w\[\033[33m\]\$(parse_git_branch)\[\033[00m\] $ "

	#export PS1="\u@\h \[\033[32m\]\w\[\033[33m\]\$(parse_git_branch)\[\033[00m\] $ "


	PS1='\[\033[0;32m\]\[\033[0m\033[0;32m\]\u\[\033[0;36m\] @ \[\033[0;36m\]\h : \w\[\033[0;32m\]$(__git_ps1)\n\[\033[0;32m\]└─\[\033[0m\033[0;32m\]▶ \$ \[\033[0m\]'




##### Install Merge Tool (diffmerge)
	
	1- download diffmerge from https://sourcegear.com/diffmerge/
	2- $ sudo apt --fix-broken install
	3- $ sudo apt-get install libcanberra-gtk-module
	4- $ sudo apt-get install libcanberra-gtk3-module
	5- $ sudo apt-get install libcurl4 -y
	6- $ sudo dpkg -i diffmerge_4.2.1.817.beta_amd64.deb
	7- $ diffmerge ( Launch diff merge tool from command line )

	
##### Configure diffmerge With Git as mergetool

	$ git config --global diff.tool diffmerge
	$ git config --global difftool.diffmerge.cmd "/usr/bin/diffmerge \"\$LOCAL\" \"\$REMOTE\""
	$ git config --global mergetool.keepBackup false
	$ git config --global merge.tool diffmerge
	$ git config --global mergetool.diffmerge.trustExitCode true
	$ git config --global mergetool.diffmerge.cmd "/usr/bin/diffmerge --merge --result=\"\$MERGED\" \"\$LOCAL\" \"\$BASE\" \"\$REMOTE\""


#### Use diffmerge as mergetool of git

	1- git difftool 		 ( check defference within current branch )
	2- git mergetool 		 ( launch merge tool as diffmerge to resalve confilict )
	3- git fetch origin feature
	4- git difftool origin/feature   ( check defference from remote branch )
	5- git merge origin/feature 	 ( merge to current branch from remote branch )

	

	
	
	
	
