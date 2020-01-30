##### Set Serminal Title
	set-title 'test'

##### Move the launcher Bottom of the screen again

	gsettings set com.canonical.Unity.Launcher launcher-position Bottom


##### Switch from path bar to location bar permanently in Nautilus

	http://askubuntu.com/questions/101100/switch-from-path-bar-to-location-bar-permanently-in-nautilus

	gsettings set org.gnome.nautilus.preferences always-use-location-entry  true


##### Associate file type with default editor

	open a file with another application using the 'mimeopen' command in the terminal
	mimeopen -d Recipes.php
	Simply choose the number that corresponds


##### cron tab

	crontab -e    	( Edit your crontab file, or create one if it doesn’t already exist. )
	crontab -l      ( Display your crontab file )
	crontab -r      ( Remove your crontab file )
	crontab -v      ( Display the last time you edited your crontab file, This option is only available on a few systems )


##### install microsoft fonts

	sudo apt-get install msttcorefonts
	use arrow key to select <ok>


##### Show Hidden Files

	Ctri + H


##### set the permissions recursively

	sudo chmod -R 777 /var/www


##### Search Command in history

	Ctrl + R


##### Install Java

	https://tecadmin.net/install-oracle-java-8-ubuntu-via-ppa/

	sudo add-apt-repository ppa:webupd8team/java
	sudo apt-get update
	sudo apt-get install oracle-java8-installer



##### Install  postman
	https://www.getpostman.com/docs/postman/launching_postman/installation_and_updates


##### MySQL Workbench
	
	https://www.linode.com/docs/databases/mysql/install-and-configure-mysql-workbench-on-ubuntu

	sudo apt install mysql-workbench

##### Downgrade firefox

	sudo apt-get purge firefox
	wget sourceforge.net/projects/ubuntuzilla/files/mozilla/apt/pool/main/f/firefox-mozilla-build/firefox-mozilla-build_39.0.3-0ubuntu1_amd64.deb
	sudo dpkg -i firefox-mozilla-build_39.0.3-0ubuntu1_amd64.deb


##### Install google Chrome

	echo "deb http://dl.google.com/linux/chrome/deb/ stable main" | sudo tee /etc/apt/sources.list.d/google-chrome.list
	wget -q -O - https://dl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
	sudo apt update
	sudo apt install google-chrome-stable

	sudo dpkg -i firefox-mozilla-build_39.0.3-0ubuntu1_amd64.deb

##### Sublime Text 3

	http://tipsonubuntu.com/2017/05/30/install-sublime-text-3-ubuntu-16-04-official-way/

	https://github.com/buymeasoda/soda-theme
	Espresso Soda ( color scheme )


##### About Linux

	HISTORY---https://en.wikipedia.org/wiki/Linux
	DESKTOP ENVIRONMENT---GUI , by which users actually interact with OS
	  1-There are many desktop environments to Linux.
		e.g. Unity, GNOME, KDE, XFCE, MATE, Cinnamon, Enlightenmentetc.
	2-GNOME-which was recently released. Beginning with Ubuntu 11.04,
		there is also the Unity shell that runs on top of GNOME 2.x
	3-GTK and Qt are user interface toolkits and frameworks.
		They are libraries that the developers use to design graphical interfaces.
		GTK and Qt are two extremely common GUI toolkits.
		GTK is the standard toolkit for GNOME while Qt is used by KDE.
	LINUX DISTRIBUTIONS--
		http://archive.oreilly.com/pub/a/linux/2005/10/27/what-is-a-linux-distribution.html
		https://en.wikipedia.org/wiki/List_of_Linux_distributions
		https://en.wikipedia.org/wiki/Linux_distribution#History
	 PACKAGE MANAGEMENT ---
	  'Software Centre' and 'Synaptic' are graphical tools whereas  'apt-get' commond line tool in Ubuntu  to manage package(software)


	


	






