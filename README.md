# Jekyll Dev Environment for Vagrant

## About

This is a simple Vagrantfile and Ansible playbook to deploy a development environment for a Jekyll powered website, such as Github Pages. Vagrant allows you to quickly build and destroy development environments, while the Ansible provisioner deploys the required packages and clones the appropriate Github repo. Out of the box, the dev environment uses VirtualBox provider, but one could edit the <code>Vagrantfile</code> for any other provider such as VMware, or EC2.

The Vagrant box used is the official CentOS release which does not include the VirtualBox guest editions, so if you prefer, you can choose a different CentOS box.

The ``./provisioning/playbook.yml` Ansible playbook deploys the following packages with Yum:

* Extra Packages for Enterprise Linux (EPEL)
* Ruby
* Ruby development packages
* Ruby gems
* NPM 
* Vim
* Git

Additionally, the playbook uses the [Github Pages](https://github.com/github/pages-gem) ruby gem, which installs all of the dependencies for GitHub Pages, matching the current running versions on the Pages platform.

## Requirements

The following software is required for a vanilla use of this dev environment:

* Vagrant - [https://vagrantup.com](https://www.vagrantup.com/)
* Ansible - [http://www.ansible.com](http://www.ansible.com/)

## Usage

1. Clone the Git repo to a local directory

        git clone https://github.com/MrThePlague/jekyll-blog-dev.git

2. Change directory to the project folder

        cd jekyll-blog-dev

3. Run `vagrant up` to build the development environment

4. Use `vagrant ssh` to connect to the development box

5. Run the Jekyll development server, and listen on the box's default IP address

        jekyll serve -H 10.0.2.15 --incremental

6. When you're finished, commit and push your changes, and then run `vagrant destroy` on your host machine to clean up!
