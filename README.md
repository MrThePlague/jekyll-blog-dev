<<<<<<< HEAD
# Cactus Theme for Jekyll

This is a port of [Cactus](https://github.com/koenbok/Cactus)'s default theme for Jekyll.
Feel free to fork, change, modify and re-use it.

## How to use it

Simply clone this repository, and then run `jekyll serve` inside the directory.
This theme is fully compliant with GH Pages and their dependencies.
For extra info: [Using Jekyll with Pages](https://help.github.com/articles/using-jekyll-with-pages/#keeping-jekyll-up-to-date).

Cactus theme includes:

* Pagination
* Rss feed
* Google Analytics Tracking code
* Code Syntax Highlight
* Author's profile with picture header
* Twitter/Facebook share buttons
* Archive posts list under each post
* Disqus comments

## Screenshots

![index page](https://raw.githubusercontent.com/nickbalestra/kactus/master/assets/images/Kactus-theme-index.png)
![post page](https://raw.githubusercontent.com/nickbalestra/kactus/master/assets/images/Kactus-theme-post.png)


## Thanks
Most of the work has been already done by the [Cactus for mac authors](https://github.com/koenbok/Cactus/blob/master/AUTHORS), I've just ported their default theme to Jekyll.
I've also added few things specific to Jekyll and some minor style changes.

## Copyright & License

Copyright (c) 2015 [Cactus Authors](https://github.com/koenbok/Cactus/blob/master/AUTHORS) -  Released under the MIT License.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
=======
# Jekyll Dev Environment for Vagrant

## About

This is a simple Vagrantfile and Ansible playbook to deploy a development environment for a Jekyll powered website, such as Github Pages. Vagrant allows you to quickly build and destroy development environments, while the Ansible provisioner deploys the required packages and clones the appropriate Github repo. Out of the box, the dev environment uses VirtualBox provider, but one could edit the <code>Vagrantfile</code> for any other provider such as VMware, or EC2.

The Vagrant box used is the official CentOS release which does not include the VirtualBox guest editions, so if you prefer, you can choose a different CentOS box.

The ``./provisioning/playbook.yml` Ansible playbook deploys the following packages with Yum:

* Extra Packages for Enterprise Linux (EPEL)
* Ruby
* Ruby development packages
* Ruby gems
* NodeJS
* NPM
* Vim
* Git

Along with the following Ruby gems:

* rdiscount
* redcarpet
* Jekyll
* Jekyll-Paginate
* Pygments

The Ruby gems installed are all the ones required for my specific blog usage; however, additional gems can be added to the playbook as required.

    - name: Install your required ruby gem
      gem: name=&lt;gem name&gt; state=latest

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

        jekyll serve -H 10.0.2.15

6. When you're finished, commit and push your changes, and then run `vagrant destroy` on your host machine to clean up!
>>>>>>> 6bded1d55947c0a92a0c6187ccac34ec585c800b
