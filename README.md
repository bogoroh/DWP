DWP
===

Deployment of web projects

<h1> Installation </h1>
First we download Git by typing:
'''sudo apt-get install git-core'''

Quickly run apt-get update to make sure that you download the most recent packages to your VPS.
'''sudo apt-get update'''

'''sudo nano ~/.gitconfig'''
You can use the follow commands to add in the required information.
'''git config --global user.name "NewUser"'''
'''git config --global user.email newuser@example.com'''

You can see all of your settings with this command:
'''git config --list'''

<h1>Add a remote </h1>
$ git remote add DWP git@github.com:bogoroh/DWP.git

<h1> Transfer the files </h1>
a. You need to add files  —> git add .

(“.” means all the files, no worries, it will add everything that was changed.)

b. You need to Commit you changes –> git commit  -m “Message you want to see near your commit”

c. Push your changes to the server –> git push
