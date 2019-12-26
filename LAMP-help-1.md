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

##### Install the Memcached

	http://www.liquidweb.com/kb/how-to-install-the-memcached-php-extension-on-ubuntu-14-04-lts/
	1- sudo apt-get install php-memcached
	OR
	sudo apt-get install php5-memcached

	2- sudo apt-get install memcached
	3- restart apache


##### Run Multiple Version of php

	https://www.tecmint.com/install-different-php-versions-in-ubuntu/
	
	sudo apt-get install python-software-properties
	sudo add-apt-repository ppa:ondrej/php
	sudo apt-get update
	sudo apt-get install php7.1
	$ sudo a2dismod php7.0
	$ sudo a2enmod php5.6
	$ sudo /etc/init.d/apache2 restart


##### Virtual Host
	1-  sudo cp /etc/apache2/sites-available/000-default.conf /etc/apache2/sites-available/test.local.conf
	2-  sudo gedit /etc/apache2/sites-available/test.local.conf 	(----- to change host name ------)
	3-  Add the content below to create a basic configuration file for the Virtual Host:

	<VirtualHost *:80>
		#ServerAdmin webmaster@test.local
		DocumentRoot "/var/www/test"
		ServerName test.local
		<Directory "/var/www/test">
			Options Indexes FollowSymLinks
			AllowOverride All
			Require all granted
		</Directory>
		#AccessFileName .htaccess
		ErrorLog "/var/www/testlogs/test.local-error_log"
		CustomLog "/var/www/testlogs/test.local-access_log" common
	</VirtualHost>

	4-  sudo a2ensite test.local ( to enable site )
	5-  sudo systemctl restart apache2
	6-  sudo gedit /etc/hosts 	( save below line for host entry)
		127.0.0.1	test.local
	


