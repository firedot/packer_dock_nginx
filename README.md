# packer_dock_nginx

Docker image built with packer

This is a Docker image built in Vagrant with packer

You could learn more about Vagrant [here](https://www.vagrantup.com/intro/index.html)

You could learn more about packer by visiting: https://www.packer.io/intro/

Information about Docker [here](https://www.docker.com/why-docker)

## Pre-requisites:

**Vagrant**
**VirtualBox**

Create the following environmental variables: 

````
export DOCKER_HUB_USERNAME="<your_dockerhub_username>"
export DOCKER_HUB_PASSWORD="<your_dockerhub_password>"

````

Clone this repository: [git](https://github.com/kikitux/xenial-docker.git) by running the following command:

````
git clone https://github.com/kikitux/xenial-docker.git
````
This will provide you with a Vagrantfile, which will bring up an Ubuntu Xenial VM with **packer**, **Docker**, and **git** installed.

Go to the repo directory.

Type:
````
vagrant up

#This will bring your VM
````

Then enter the machine by typing:

````
vagrant ssh
````
You are now connected to the virtual machine.

### Packer phase

Clone this repository by typing:

````
git clone https://github.com/firedot/packer_dock_nginx.git
````

Go to the cloned repo dir.

Run the following line:

````
packer build docker_template.json
````
This line will generate a Docker image and will upload it to the Docker Hub.


