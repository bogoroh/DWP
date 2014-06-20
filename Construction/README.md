DWP
===

Deployment of web projects

## Installation
First we download Git by typing:

	sudo apt-get install git-core

Quickly run apt-get update to make sure that you download the most recent packages to your VPS.
	
	sudo apt-get update
	sudo nano ~/.gitconfig
You can use the follow commands to add in the required information.

	git config --global user.name "NewUser
	git config --global user.email newuser@example.com

You can see all of your settings with this command:
	
	git config --list

Install apache 2
	
	sudo apt-get install apache2
	sudo service apache2 restart
	pico /etc/apache2/conf.d/security

* Add ServerName localhost


## Add a remote 

	$ git remote add DWP git@github.com:bogoroh/DWP.git

## Transfer the files
1. You need to add files  —> git add "."

	* (“.” means all the files, no worries, it will add everything that was changed.)

2. You need to Commit you changes –> git commit  -m “Message you want to see near your commit”

3. Push your changes to the server –> git push

4. Pull your changes from your github -> git pull "remote" "branch"


## Git hooks
Create Space for Repo on Live Server

	sudo mkdir /var/repos/ 
	sudo chown YourUserName /var/repos
	cd /var/repos && mkdir SiteName.git && cd SiteName.git
	git init --bare


Setup server hooks

	cd /var/repos/SiteName.git/hooks/
	pico post-receive
		#!/bin/sh
		GIT_WORK_TREE=/var/www git checkout -f

	(Optional) If you are using multiple domains on one server and followed the Apache Multiple Virtual Host Instructions.

Give permissions to make the hook executable by the server

	chmod +x hooks/post-receive


Configure Local Dev Environment
	
	mkdir ~/Projects
	mkdir ~/Projects/SiteName.com && cd ~/Projects/SiteName.com 
	git init
	git remote add prodServer ssh://YourUserName@IPAddress/var/repos/SiteName.git

Once you're done you keep committing your changes and once you are ready to push the commits to the live server.


### Credits
Mike Taatgen