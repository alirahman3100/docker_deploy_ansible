# docker_deploy_ansible
# Steps for Ansible Docker Container 

Firstly install WSL Linux Subsystem on Window Machine.
After that I install Ubuntu VM on Vitual Box.
IP of my Ubuntu VM is 192.168.0.107
Then install ansible on WSL using command sudo apt install ansible
and install Docker on Ubuntu VM.
Then make a directory in wsl using commnad mkdir ansible_project
Using command cd ansible_project we entered into this directory.
In this directory I make Ansible-Playbook using command sudo nano docker_deploy.yml
Also in this directory I make a file name hosts in which you add IP address of VM on which Docker is installed.
In this playbook I define host, tasks and network on which apache container is running.
The given Network for Apache Docker Conatainer is 172.168.10.0/30
After that we run this Ansible Playbook using coomand ansible-playbook -i hosts docker_deploy.yml
It runs successfully and to ensuring the Network of Docker Container I run command ip addr show on Ubuntu VM
And after that i run the http://192.168.0.107:80 on browser to ensure that our Apache working or not.
And it works!!!
