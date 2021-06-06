# Docker Ansible Playbook

This project aims to demonstrate the Ansible capabilities when you need to provision multiple Docker machines in a few steps.

## Prerequisites

Software that needs to be present on your local machine:
- A recent version of Ansible
- A recent version of Vagrant
- A recent version of Libvirt or VirtualBox

## First startup

~~~
vagrant up
~~~

## Miscellaneous

### Visual Studio Code used extensions

~~~
ms-vscode-remote.remote-ssh
zbr.vscode-ansible
bbenoist.vagrant
redhat.vscode-yaml
~~~

### Commands

~~~
vagrant box add centos/7    ---> choose libvirt/virtualbox ----> it downloads vagrant box in advance
vagrant init centos/7       ---> creates the initial Vagrantfile
vagrant up                  ---> start/provision for the first time
vagrant halt                ---> stop
vagrant destroy             ---> delete the machine from libvirt
vagrant provision           ---> run the provisioner again
~~~