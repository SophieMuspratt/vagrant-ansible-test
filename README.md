# DevOps Graduate Test

This project is my attempt at the devops grad test:

Your challenge is to write a piece of automation to run against a remote Ubuntu server. This should patch the server, reboot the server, and display the servers up time. This can be written using any tooling of your choice. Your development should be submitted under source control.

# Setting up the environment
The environment needed so I could attempt this challenge was set up by Mike Ruocco using VirtualBox, Unyntu and Vagrant.
Notes from Mike:
In order to make the project easily runnable I have used vagrant to provision both a ubuntu desktop machine (the control machine that the automation can be run from) and
a ubuntu server (the remote machine that should be patched and rebooted by the automation.) 

# Setting up the vagrant virtual machines

You should be able to set up the two virtual machines described above by running the following command:

```
vagrant up
```

Once that completes you should have a ubuntu desktop machine (control) and a ubuntu server (remote.) You can log into the desktop/control machine using vagrant as both
the username and password. Once you have logged in you should be able to run the automation by running the following commands:

```
cd ansible-test
ansible-playbook devops-test.yml -i inventory
```
#NOTE!
Please be patient when running devops-test.yml, It takes a while to run the Upgrade Packages Task but will complete it!
