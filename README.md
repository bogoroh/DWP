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

## Add a remote 

	$ git remote add DWP git@github.com:bogoroh/DWP.git

## Transfer the files
a. You need to add files  —> git add .

(“.” means all the files, no worries, it will add everything that was changed.)

b. You need to Commit you changes –> git commit  -m “Message you want to see near your commit”

c. Push your changes to the server –> git push

### Credits
Mike Taatgen