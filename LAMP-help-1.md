#### Remove/Uninstall LAMP

	https://www.sumitbera.com/completely-uninstall-php-and-mysql-at-ubuntu/
	
	sudo apt-get remove –purge php*
	sudo apt-get purge php*
	sudo apt-get autoremove
	sudo apt-get autoclean
	sudo apt-get remove dbconfig-php
	sudo apt-get dist-upgrade

	sudo apt-get remove –purge mysql*
	sudo apt-get purge mysql*
	sudo apt-get autoremove
	sudo apt-get autoclean
	sudo apt-get remove dbconfig-php
	sudo apt-get dist-upgrade.
	
	
	sudo apt-get remove –purge apache*
	sudo apt-get purge apache*
	sudo apt-get autoremove
	sudo apt-get autoclean
	sudo apt-get remove dbconfig-php
	sudo apt-get dist-upgrade.

#### Install LAMP ON Ubuntu 18.04

	https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-ubuntu-18-04

	sudo chmod -R 777 /var/www		( Recursive write Permission )	
	sudo a2enmod rewrite			( Load rewrite modile )
	sudo /etc/init.d/apache2 restart	( restart apache )	

##### Check Loaded Module of Apache

	apache2ctl -M

##### Install curl

	sudo apt-get install curl
	curl --version    ( check version )

##### Install lDap module of php
	
	sudo apt-get install php7.0-ldap
	sudo /etc/init.d/apache2 restart ( restart apache )


##### Additional PHP modules

	sudo apt install php-curl php-gd php-mbstring php-mcrypt php-xml php-xmlrpc php-json
