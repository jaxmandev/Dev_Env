## Vagrant

- vagrant is a tool used by devops engineers to help build and configure virtual enivronments.
- vagrant features can be broken down into a few key areas:
- vangrantfile
1. boxes
2. networking
3. provisioning
4. plugins

## vagrantfile
```
- a vagrantfile is a configuration file that uses Ruby programming language syntax.
- it is easy to understand and can be quickly tested by making a change and then running the vagrant up to see whether the expected results have been implemented
- vagrantfiles can easily be shared and added into version control.
- its lightweight and contains everything needed for another user to replicate a virtual environment/application
```
## Provisioning
```
- Provisioning in Vagrant is a way to configure the vagrant machine.
- Through provisioning you are able to install software dependencies as the machine is being created.
```
## Advantages of Vagrant
```
- Vagrant allows you the user to easily package up a virtual environment that can be shared with other developers.
- These virtual environments can be configured to match the production environment of the application/code is running
- This can help minimise the presence of bugs/errors when the code is deployed to the production environment
a big advantage of vagrant is the vagrant configuration file known as vagrantfile can be easily created, edited and tested.
- The syntax of a vagrantfile is easy to understand and offers a simple way to build complex virtual environments
```
## Vagrant and Developers
```
- Vagrant gives access to developers to package up their code/application into an easily sharable fully-fledged development environment.
- This can then be used by other developers who do not have the original production environment and are using different OS such as Linux, Windows or macOS.
```
## Vagrant and Operations
```
- The operations team can easily and quickly test deployment tools and scripts using vagrant.
- Vagrant supports many popular deployment tools such as: Docker, Puppet and Chef.
```