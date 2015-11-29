#Getting Started
1. Install Virtualbox - http://download.virtualbox.org/virtualbox/4.3.18/VirtualBox-4.3.18-96516-OSX.dmg
2. Install Vagrant - https://dl.bintray.com/mitchellh/vagrant/vagrant_1.6.5.dmg
3. Install Ansible - https://devopsu.com/guides/ansible-mac-osx.html or `brew install ansible` if you use Homebrew (http://brew.sh/)
3. Clone this repo
4. Go into the repo
5. To start your new dev environment run 'vagrant up'.  This will take several minutes to create and provision the virtual machine.
6. To ssh to your new dev environment run 'vagrant ssh'
7. For more information on Vagrant see http://docs.vagrantup.com/v2/

#What's inside
1. Fedora 20 fully patched
2. MySQL/MariaDB Server, Git, and Vim installed
3. RVM with Ruby 2.1.4

#MySQL/MariaDB Info
Root password is blank.

#Connecting
- Guest IP is 192.168.33.11
- vagrant ssh
- ssh vagrant@192.168.33.11 (password is 'vagrant')

#License
Released under the [MIT License](http://www.opensource.org/licenses/MIT).
