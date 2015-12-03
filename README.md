# Getting Started
1. Install Virtualbox - https://www.virtualbox.org/wiki/Downloads
2. Install Vagrant - https://www.vagrantup.com/downloads.html
3. Install Ansible - `brew install ansible` or https://devopsu.com/guides/ansible-mac-osx.html
3. Clone this repo - `git clone git@github.com:irlrobot/fedora_dev.git`
4. Go into the repo - `cd fedora_dev`
5. To start your new dev environment run `vagrant up`.  This will take several minutes to create and provision the virtual machine.
6. To ssh to your new dev environment run 'vagrant ssh' and its IP is 192.168.33.33
7. For more information on Vagrant see http://docs.vagrantup.com/v2/

## Sizing
By default the virtual machine will have 2 CPU's and 2048MB of RAM.  If you'd like something with better performance at the expense of using more system resources you can either edit the Vagrantfile and adjust the values for memory and cpu, or start the virtual machine with `VMSIZE='auto' vagrant up` which will give the virtual machine 1/4 of your total system RAM and the same number of CPU's as the host machine.

You can set a shell export with this variable for convenience (`export VMSIZE='auto'` inside .bashrc or .zshrc, for example).

## Guest Additions
You can optionally install the VirtualBox Guest Additions by executing the below from your directory where the Vagrantfile is:
```
vagrant plugin install vagrant-vbguest
```

See https://github.com/dotless-de/vagrant-vbguest for more info.

# What's inside
1. Fedora 22 fully patched
2. MySQL/MariaDB Server, Git, and Vim installed
3. RVM with Ruby 2.2.3

# MySQL/MariaDB Info
Root password is blank.

# Connecting
- Guest IP is 192.168.33.11
- vagrant ssh
- ssh vagrant@192.168.33.11 (password is 'vagrant')

# Installation Notes
If you are having trouble completing provisioning, this setup is known to work with the following versions so please try one of these:

## Ansible
- 1.7.2
- 1.9.4

## Vagrant
- 1.6.5
- 1.7.2
- 1.7.4

## Virtualbox
- 4.3.20 r96996
- 4.3.26 r98988
- 5.0.10 r104061

## NFS
The Vagrantfile is setup to use NFS by default to improve performance.  If you're using OS X and having an issue with timeouts when mounting the NFS shared folder try rebooting your Mac.  You can disable NFS and use the native Vagrant mounting by commenting out line 36 in Vagrantfile.

To avoid being prompted for sudo credentials each time you `vagrant up`, have a look at https://docs.vagrantup.com/v2/synced-folders/nfs.html and the "ROOT PRIVILEGE REQUIREMENT" section.

# License
Released under the [MIT License](http://www.opensource.org/licenses/MIT).
