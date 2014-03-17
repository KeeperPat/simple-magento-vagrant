simple-magento-vagrant-with-ansible
======================

A simple Magento environment provisioner using [Ansible](http://www.ansible.com/home) and [Vagrant](http://www.vagrantup.com/).

* Creates a running Magento development environment with a few simple commands.
* Runs on Ubuntu (Precise 12.04 64 Bit) \w PHP 5.3, MySQL 5.5, Apache 2.2
* Uses [Magento CE 1.8.1.0](http://www.magentocommerce.com/download)
* Automatically runs Magento's installer and creates CMS admin account.
* Automatically runs [n98-magerun](https://github.com/netz98/n98-magerun) installer. 
* Perfect for rapid development or extension testing with an unopionionated, bare-bones and easily tweaked configuration.
* Goes from naught-to-Magento in a couple of minutes.

## Getting Started

**Prerequisites**

* Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
* Install [Vagrant](http://www.vagrantup.com/)
* Install [Ansible](http://docs.ansible.com/intro_installation.html#installation)
* Clone or [download](https://github.com/KeeperPat/simple-magento-vagrant/archive/master.zip) this repository to the root of your project directory `git clone https://github.com/KeeperPat/simple-magento-vagrant.git`
* In your project directory, run `vagrant up`

The first time you run this, Vagrant will download the bare Ubuntu box image. This can take a little while as the image is a few-hundred Mb. This is only performed once.

Vagrant will use Ansible to configure the base system before downloading Magento and running the installer.

## Usage

* In your browser, head to `127.0.0.1:8080`
* Magento CMS is accessed at `127.0.0.1:8080/admin`
* User: `admin` Password: `password123123`
* Access the virtual machine directly using `vagrant ssh`
* When you're done `vagrant halt`

[Full Vagrant command documentation](http://docs.vagrantup.com/v2/cli/index.html)

## Todo
* Expose MySQL port for access using Workbench or your preferred MySQL admin tool.
* Install Modman.
* Optionally install sample store inventory

