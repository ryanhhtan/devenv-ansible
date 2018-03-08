# My Dev Enviroment

## Description
This is a Vagrant + ansible project to create a LEMP stack developing enviroment for personal usage.
L: Ubuntu 16.10
E: Nginx
M: Mysql server
P: PHP

## Usage 
### Prerequists:
1. Virtualbox
2. Vagrant

### Steps
1. Clone the project.
2. Roles ssh-in and git-client requires ssh id_rsa file which is not stored in the repo for security concern. Add the keys in the role's file directory with extension "secret" which is ingored from uploading to the repo. 
3. Run "vagrant up" to start the virtual environment.
