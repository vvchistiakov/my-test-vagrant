# my-test-vagrant
This is skeleton for CentOS7 by vagrant.
After when VM will be installed, you can find this git project directory in synced folder /opt/<project name> in VM.

## Build on your Laptop
 * [Install Vagrant](https://www.vagrantup.com/downloads.html)
 ```bash
 brew cask install vagrant
 ```
 * [Install VirtualBox](https://www.virtualbox.org/wiki/Downloads)
 ```
 brew cask install virtualbox
 ```
 * Install Vagrant plugin for VirtualBox 
 ```bash
 vagrant plugin install vagrant-vbguest
 ```
 * Add CentOS 7 image for VirtualBox 
 ```
 vagrant box add centos/7
 ```

 ### Go to build place
 * Clone the Git project for your workmachine
 * Join into directory with the project
 * Generate SSH key
 if this is first vagrant installation, you shoul generate special shh key for access to virtual machines which will provision by Vagrant. Please will run this command if `~/.vagrant.d/insecure_private_key` doesn't exist.
 ```
 ssh-keygen -f ~/.vagrant.d/insecure_private_key
 ```
 * Build your Vagrant VM.
 ```
 vagrant up
 ```
 * Connect to your builded VM.
 ```
 vagrant ssh
 ```