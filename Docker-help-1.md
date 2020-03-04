########## Reference #############################
	https://semaphoreci.com/community/tutorials/dockerizing-a-php-application
	https://dev.to/johnmccuk/isolating-php-with-docker-containers-4epn
	https://www.javatpoint.com/docker-php-example
	https://docs.docker.com/samples/library/php/
	https://www.tecmint.com/install-apache-web-server-in-a-docker-container/


	https://bitpress.io/simple-approach-using-docker-with-php/ ( ** )
	https://alysivji.github.io/php-mysql-docker-containers.html
	https://github.com/t3kit/ubuntu18.04-php7.2-apache/blob/master/Dockerfile ( ** )
	https://tech.mybuilder.com/virtual-hosts-with-docker/ ( ** )
	
	--- docker-compose---
	https://docs.docker.com/compose/install/	
	https://takacsmark.com/docker-compose-tutorial-beginners-by-example-basics/ (docker-compose.yml)
	https://blog.codeship.com/orchestrate-containers-for-development-with-docker-compose/

	https://www.howtoforge.com/tutorial/ubuntu-docker-portainer/
	https://www.linuxtechi.com/monitor-manage-docker-containers-portainer-part1/

#### Why Use Docker
	https://ropenscilabs.github.io/r-docker-tutorial/01-what-and-why.html
	https://www.youtube.com/watch?v=wi-MGFhrad0&list=PLhW3qG5bs-L99pQsZ74f-LC-tOEsBp2rK&pbjreload=10

#### Installation
	https://www.tecmint.com/install-docker-and-run-docker-containers-in-ubuntu/
	https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-16-04
	https://docs.docker.com/install/linux/docker-ce/ubuntu/

	

#### run docker commands without sudo
	1- sudo groupadd docker
	2- sudo usermod -aG docker $USER
	3- restart system / Log out and log back in so that your group membership is re-evaluated.
	4- Verify that you can run docker commands without sudo.

#### Basic Commands
	docker --version
	docker info
	docker build -t <IMAGE NAME> <docker-file-location>   Build Docker Image from a Dockerfile 
	docker run -d <IMAGE NAME>  			      Run Docker Image (-d : It is used to create a daemon process)
	docker images                        		      List the image that was downloaded to your machine
	docker ps -a / docker container ls -a                 List all container	
	docker rm <CONTAINER ID>	                      Remove Docker Containers
	docker rmi <IMAGE ID>                                 Remove Docker Images
	docker rm $(docker ps -a -q)                          Remove All Containers
	docker rmi  $(docker images -q)                       Remove All Images
	docker stop $(docker ps -a -q)                        Stop All Containers
	docker logs -f <CONTAINER ID>
	docker start <CONTAINER ID>
	docker exec -it <CONTAINER ID> bash                   Enter into Docker container
	docker-compose up / docker-compose up --build
	
********************************************************************************************************

	docker image -> is described in text file called a Dockerfile, which has a simple and well-defined syntax.

	Dockerfile   -> is a text document that contains commands that are used to assemble an image.

	Create Docker Image with image name -> 
		docker build -t image-name docker-file-location (-t : to tag Docker image with the provided name)
		docker build -t my-php-img -f ./Dockefile . (if Dockerfile in current dir)
		docker build -t my-php-img . (if Dockerfile in current dir)

	Dockerfile Instructions ->
		1- instructions are not case-sensitive but you must follow conventions which recommend to use uppercase.
		2- first instruction must be FROM in order to specify the Base Image.
		3- statement begin with # treated as a comment.

	FROM  -> is used to set the Base Image for the subsequent instructions. A valid Dockerfile must have FROM as its first instruction.
		FROM ubuntu:18.04

	LABEL -> add labels to an image to organize images of our project.
		LABEL vendorl = "JavaTpoint"  

	RUN -> This instruction is used to execute any command of the current image.
		RUN apt-get update && apt-get install -yq --no-install-recommends \
		    apt-utils \
		RUN apt-get install -y apache2
		RUN apt-get install -y libapache2-mod-php7.2
		RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

	CMD ->  This is used to execute application by the image, 
		There can be only one CMD in a Dockerfile. If we use more than one CMD, only last one will execute.
		CMD ["executable", "param1", "param2"?]  
		CMD apachectl -D FOREGROUND 
	
	COPY -> This instruction is used to copy new files or directories from source to the filesystem of the container at the destination.
		COPY typo3.conf /etc/apache2/sites-available/
		COPY . /var/www/html

	WORKDIR -> The WORKDIR is used to set the working directory for any RUN, CMD and COPY instruction that follows it in the Dockerfile.
		WORKDIR /var/www/html  
		
		 
		

#######################################################################################################


	1- $ cd /home/bajpjai/php-projects
	2- $ mkdir app1
	3- $ cd app1
	4- put your code inside app1 directory
		// index.php   <?php echo  'come here'; ?>
	5- // Dockefile
		FROM php:7.2-apache
		COPY . /var/www/html
	
	6- Create Docker Image with image name
		$ docker build -t my-php-img .
		OR
		$ docker build -t my-php-img -f ./Dockefile .
		OR
		docker build --no-cache -t my-php-img -f ./Dockefile .
	7- Run the Docker image
		$ docker run my-php-app ( Need build again, if change in code )
		OR
		docker run -v /home/bajpjai/app1:/var/www/html my-php-app ( No need build again, if change in code )
		OR
		nohup docker run -v /home/bajpjai/Desktop/php-docker-app:/var/www/html php-app-img & (run image in background )
		  

	8- checking running container (container is a running instance of a image)
		$ docker ps
	
	9- stop container 
		$ docker container stop 86db764cdfd6



########################################################################################################

	
