![Vagrant by Hashicorp](https://www.vagrantup.com/vagrant/img/logo-hashicorp.svg)
# Multi VM Setup!

This is a vagrant vm automation script to setup multiple vms (Ubuntu 20 and CentOS 7), install simple web servers, deploy sample websites from https://tooplate.com  accessible from the local ip address **192.168.62.13** and **192.168.62.14**.

# Requirement

Familiarity with linux operating system and vagrant.

## Commands

**vagrant up** - Setup the linux vm, install required softwares, download html template and serve the templates on respective ip addresses **192.168.62.13** and **192.168.62.14**.

**vagrant ssh web01** - Login the web01 (ubuntu) vm as super user.

**vagrant ssh web02** - Login the web02 (centos) vm as super user.

**vagrant halt web01** - Power off web01(ubuntu) vm.

**vagrant halt** - Power off all linux vms.

**vagrant destroy** - Destroy linux vms