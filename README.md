# Automated installation of Wordpress on Ubuntu 14.04

## Introduction

This is ansible playbook created based on manual from:
https://www.digitalocean.com/community/tutorials/how-to-install-wordpress-on-ubuntu-14-04
All roles are based on chapters from manual excluding first one called "lamp"
which is installing LAMP set of software to continue with wordpress and "stepfive" wich require
creating wordpress user in browser and does not exist as a role. 

## Versions

The playbook was build on Ubuntu 14.04 using Ansible 2.4.1.0 and tested using same environment

## Variables

Folders users permissions and DB user settings can be edited in defaults/main.yml

## Before you start

Please edit hosts file located in the root folder of playbook. 
Please add ip addresses or hostnames of machines you want wordpress to be installed to. 
File should look like this:

```
[wordpress]
192.168.0.20
192.168.0.21
```
## Running playbook

Run: ansible-playbook playbook.yml -b -u ben -K
Where ben is user with sudo rights on remote machines and -K flag means that user password will be asked after executing the playbook.

## P.S. 
This is my first playbook on ansible so code could look like a porn.

