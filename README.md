# ANSIBLE

# Ubuntu VM IPS

## Ubuntu Ansible 
192.168.1.52

## Ubuntu VMs
ubuntusrv1: 192.168.1.71
ubuntusrv2: 192.168.1.8
ubuntusrv3: 192.168.1.127
grafanavm: 192.168.1.184



# Useful commands

## Generate SSH key
ssh-keygen

## Copy SSH key to server
ssh-copy-id -i ~/.ssh/-keyfile- -ip.of.the.server-

## Add passphrase to ssh-agent
ssh-add
> enter password

## Alias for SSH agent
alias ssha='eval $(ssh-agent) && ssh-add'

## Edit .bashrc
nano/vi .bashrc

# GIT commands
git add FILE.ext
git status
git commit -m "commit message"
git push origin main

git config --global user.name "Cameron Robbins"
git config --global user.email "cammrobb@gmail.com"

# Ansible commands
ansible all --key-file ~/.ssh/ansible -i inventory -m ping
ansible all --list-hosts

> Gather facts for VMs
ansible all -m gather_facts 

> Update apt cache
ansible all -m apt -a update_cache=true

> Upgrade
ansible all -m apt -a upgrade=yes

> Flag to limit to a single device
--limit ip.ad.dr.ess

> run elevated commands
--become --ask-become-pass

> when
when: ansible_distribution == "Distro"

when: ansible_distribution in ["Debian", "Ubuntu"]


USE GETS FACTS TO CREATE A TXT FILE

USE PYTHON TO PULL RELEVANT INFO OUT TEXT FILE 

CREATE ASSET REGISTER?