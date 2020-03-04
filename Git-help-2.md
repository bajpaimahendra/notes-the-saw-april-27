

##### frequently used commands

	git status
	git checkout -b  feature1 master 	( Create a new branch from another branch )
	git checkout -- <file-path>		( revert local change)
	git chechout branch-name		( swithch to another branch )
	git git add <file-path> / add . 	( Add one or more files to staging (index) )
	git commit -m'message'			( commit added files )
	git push origin branch-name / git push origin -u branch-name / git push origin -f branch-name
	git merge feature1
	git mergetool


##### Viewing unpushed Git commits

	git log origin/master..HEAD
	
	You can also view the diff using the same syntax
	
	git diff origin/master..HEAD
	
#### delete a Git branch locally

	git branch -d <branch_name>
	git branch -D <branch_name> 	(-D, which is an alias for --delete --force ) 
	

#### delete a Git branch  remotely
	
	git push -d <remote_name> <branch_name>
	git branch -d <branch_name>

##### Create a new branch from another branch
	
	git checkout -b  feature1 master

##### .gitignore is now working


	git rm -r --cached .	( rm all files )
	git add .		( add all files as per new .gitignore )
	git commit -m ".gitignore is now working" ( now, commit for new .gitignore to apply)

##### Track newly create remote branch

	git fetch --all
	git branch --track branch-name origin/branch-name

##### Change origin

	git remote set-url origin https://mahendravrn@bitbucket.org/visitatvishal82/tawarmall.git


##### Operation

	1- git init  or git clone

	2- git status 			( status of current branch )

	3- git fetch origin feature1

	4- git difftool origin/future1   ( check defference from current branch )

	5- git merge origin/future1 ( merge to current branch from remote branch )

	6- git mergetool ( launch merge tool to resalve confilict )

	7- git push <remote> <branch>	( push perticula branch to remote repositry )
		git push origin develop 
		git push -u origin develop (first time only to set upstrem)
	 
	8- git checkout develop  ( swithch to branch )


######################################################################################################################################


manage-booking-mak-7

Old File

b2c/config/autoload.php
b2c/helpers/utilflight_helper.php
b2c/views/template_list/template_v1/report/airline.php
b2c/views/template_list/template_v1/report/print_book.php

New File
system/helpers/custom/common_helper.php


if($CurrentStatus=='BOOKING INPROGRESS'){
   echo 'jmd...';
}


test1@gmail.com  / FB1102202009424407
bajpai@gmail.com / mahendra.bajpai@gmail.com FB1102202011368271

$bookings['booking_details'][0]['status']

booking_transaction_details

FB1302202006001102



CREATE TABLE tbo_city_list (
id INT(6) UNSIGNED AUTO_INCREMENT PRIMARY KEY,
iso_alpha_2_country_code VARCHAR(30) NOT NULL,
city_name VARCHAR(200) NOT NULL,
city_code int(50)

)













