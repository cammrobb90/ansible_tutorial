# ANSIBLE

# Ubuntu VM IPS

## Ubuntu Ansible 
192.168.1.52

## Ubuntu VMs
192.168.1.71
192.168.1.8
192.168.1.127

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
ansible all -m gather_facts --limit ip.ad.dr.ess
