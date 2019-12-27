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
	git config core.fileMode false					   ( inside project dir )

##### Show Current  Branch In Terminal	

	paste below code at the end of file /home/bajpai/.bashrc
		
	parse_git_branch() {
	  git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
	}

	#export PS1="\u@\h \[\033[33m\]\$(parse_git_branch)\[\033[00m\] ${debian_chroot:+($debian_chroot)}\w $ "

	#export PS1="\u@\h \[\033[32m\]\w\[\033[33m\]\$(parse_git_branch)\[\033[00m\] $ "

	#export PS1="\u@\h \[\033[32m\]\w\[\033[33m\]\$(parse_git_branch)\[\033[00m\] $ "


	PS1='\[\033[0;32m\]\[\033[0m\033[0;32m\]\u\[\033[0;36m\] @ \[\033[0;36m\]\h : \w\[\033[0;32m\]$(__git_ps1)\n\[\033[0;32m\]└─\[\033[0m\033[0;32m\]▶ \$ \[\033[0m\]'






