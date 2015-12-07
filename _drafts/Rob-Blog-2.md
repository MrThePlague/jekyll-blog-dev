---
title:  "Blog 2.0"
description: Work in progress
## date: add a date when publishing
---

# A Fresh Start

After originally starting the first incarnation of this blog a few years ago, I managed a whopping two posts before life got in the way.
I decided recently to restart the initiative, and have another go at putting something of substance down on _paper_. Even if not one person reads anything I publish, the process of writing and externalizing what I'm learning will help me remember, and provide a personal reference of sorts.

# Platform

RobBlog 1.0 was built on a public Wordpress platform, from a hosting provider of which I had no intention of a continued relationship.
When I was searching for a new platform, I was looking for something that would be simple to maintain, customizable, and where posts could be written in Markdown. After reading a great [blog post by Scott Lowe](http://blog.scottlowe.org/2015/01/06/the-story-behind-the-migration/), I decided to look into using [GitHub Pages](https://pages.github.com) and [Jekyll](http://jekyllrb.com) as the foundation for RobBlog 2.0.
Without going into too much detail, Jekyll allows you to build a blog using a combination of Markdown and YAML, which is highly appealing to someone that doesn't want to go down the web development rabbit-hole, ie: me.

# Dev Environment

Once I'd made the decision on my Blogging platform, I realized that I'd like to build a development environment for working on the Blog itself. After years of use, my laptops had become slightly cluttered with multiple versions of Ruby, directory bloat, and so on. I therefore came to the conclusion that I would like a keep a clean slate and just focus on the Blog itself, and not managing the various packages and potential conflicts on my host machines. Also, as move between two different computers regularly, it would be nice to share the same environment between the two workstations, and maintain a consistent workflow.

I was already a user of both [Vagrant](https://www.vagrantup.com) and [Ansible](http://www.ansible.com), so it was an easy decision to incorporate these two pieces of software into the creation of a _mobile blogging workstation_.


# GitHub

The first step in creating the development environment was to create a new GitHub project

# Vagrant

I've made the assumption at this point that the reader already has a little bit of familiarity with Vagrant, but in a future blog post I'll discuss a bit more about the ins and outs of this fantastic piece of software.

The first step in creating the development environment was to create a new Vagrant project with the provider and the default Vagrant box. This simply creates a generic Vagrantfile in the directory, which can be edited to suit. Alternatively, you could write a Vagrantfile from scratch, we've taken the easy route here to get going.

    $ mkdir <directory to use>


# Ansible


# GitHub Pages


# Next Steps














