#### Installing Node through NVM (Node version manager) ---
	NVM is used to control and manage multiple active versions of Node.js in one system
	1- sudo apt-get update					                                        (packages are up to date)
	2- sudo apt-get install build-essential libssl-dev	                                        (The build-essential package (C++ Compiler) 
	3- curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash		(start the installation script)
	4- Close and reopen your terminal to start using nvm
	
	$ nvm --version	
	$ nvm ls-remote	      (To find out the versions of Node.js that are available for installation)
	$ nvm install node    (install the latest Node.js version)
	$ nvm install 8.11.2  (Install Node , NPM will automatically install) 

	$ node -v	      (check node version) 
	$ nvm ls	      (List Node.js versions which are installed)

	https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-16-04
	https://www.liquidweb.com/kb/install-nvm-node-version-manager-node-js-ubuntu-16-04-lts/
	https://github.com/creationix/nvm	
	https://www.sitepoint.com/quick-tip-multiple-versions-node-nvm/

#### V8  Engine -----

    1- An interpreter which executes JavaScript code into machine code
    2- open source, developed by Google, written in C++
    3- This engine is used inside Google Chrome
    4- V8 is also used for the popular Node.js
	
#### Nodejs ---

    1- written in C++
    2- use v8 engine
    3- open source
