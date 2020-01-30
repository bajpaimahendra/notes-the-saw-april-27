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

	
	
	

	
	
	
	
