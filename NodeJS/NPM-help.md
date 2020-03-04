#### NPM (will automatically install with Node) -----------------------
	npm init 	(to initialize package.json)

	npm install  moduleName --save	( -- save write in package.json if not alaready available )
		npm express install --save
	npm install express 	( install express 3.0 module globally) 
	sudo apt install node-express-generator	( install express 4.0 module globally for each node project)
	 
	express ProjectName ( create project and package.json through express global module)

	npm install

	------------------------
	jade@1.3.1: Jade has been renamed to pug, please install the latest version of pug instead of jade


	npm uninstall jade --save
	then

	npm install pug --save 
#### List all package which are installed globally
	$ npm list -g --depth=0

#### Uninstall package which are installed globaly------
	$ npm uninstall -g <packageName
	$ npm uninstall -g json-concat
