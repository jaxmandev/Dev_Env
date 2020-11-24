## First Virtual Box and Vagrant Dev Environment

### Virtual Box

- Virtual box is an open source hosted hypervisor used for the purposes of virtualisation.
- Virtualisation is the creation of a virtual object such as an operating system, server, storage etc.
- With virtualisation, a guest OS is abstracted away from the underlying hardware or software. A hypervisor is a tool used to achieve virtualisation.
- A hypervisor is a layer of software which emulates the underlying hardware of a physical resource and separate the constituents so they can be used by the virtual environment.
- While the performance of a virtual machine is not comparable to an actual computer, it is usually sufficient as a virtual machine does not need all the functionality of the base computer.
### Vagrant

- Open source Linux distribution
- Written in ruby
- Vagrant boxes - preloaded vagrant files that create virtual machines. - Usually just an OS.
```
The easiest way of adding a box is looking up from the catalog. There are many boxes available including ubuntu.
```
- Ubuntu is an open source OS. It is available as a:
- Ubuntu with GUI (graphical user interface) looks and works like a standard desktop
- Ubuntu headless - basically a terminal, no GUI (this is the one we will use)
```
faster
more secure
lighter
```
### Main Commands

#### General Commands
```
vagrant init - Creates a vagrantfile based on a box in the Vagrant Cloud. This command can also be run as follows:
vagrant init <box> - initialises a specific box
vagrant up - get the box to run.
vagrant destroy - delete a box- everything inside is lost
vagrant ssh - login to the virtual machine
logout - log out of the virtual machine
vagrant suspends - saves contents of box
```
#### Bash Commands

By running the vagrant ssh command, we login to the virtual machine and can run bash commands such as:

```
mkdir - create a new directory
nano - create a new file
cd - go to a directory
ls - view files
rm - delete a file
rm -rf - delete a folder
pwd - prints the current working directory
cat - view the contents of a file
sudo apt-get update - updates the source list. 
sudo is used to give administrative rights and apt-get is the package installation manager for linux.
```
### Task 1
```
1. Create a new virtual machine with ubuntu xenial64 i.e vagrant up
1. Confirm the machine is running in VirtualBox, then destroy using vagrant destroy
1. Delete your vagrantfile
1. Use vagrant init to create a new vagrantfile utilising centos 7
1. Run the new virtual machine using vagrant up
1. Confirm the new machine is running then vagrant destroy again.
```
### Task 2
```
1. Create a vagrant box with ubuntu version 18.04
1. Find the command to ssh into machine and do so
1. Create a README.md file inside the virtual machine and write your name and favourite movie.
```
#### Deployment
- NGINX is a high performance load balancer used to deliver content to the web. We download this in our virtual machine using the command `sudo apt-get install nginx'
```
- We then add the following line to our vagrantfile to configure a private network. config.vm.network "private_network",ip:"192.168.10.2"
Using an ip address is not convenient nor standard practice. We typically access using a domain name. 
- We can alias a domain name by using the following command inside our terminal, ensuring we have logged out of the virtual machine. vagrant plugin install vagrant-hostsupdater
- We then alias a domain name as demonstrated below: config.vm.hostname = "www.testing.de"
```