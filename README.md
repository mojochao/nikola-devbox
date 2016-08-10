# Nikola Blog Infrastructure Project

## Overview

This repo provides the infrastructure necessary for authoring static
sites with [Nikola](https://getnikola.com/) and deploying them to a
server.

## Installation

This project provides a vagrant linux vm (ubuntu 16.04 LTS) provisioned
for use with Nikola, called *nikola-devbox*.

> $ git clone xxx
> $ cd nikola-devbox
> $ vagrant plugin install vagrant-vbguest
> $ vagrant up
> $ vagrant ssh
> ubuntu@nikola-devbox:~$ 

You are now connected to the *nikola-devbox* vm.  The **sites**
subdirectory is mounted in the vm under your home directory.  You
should perform all content work in that directory.

> ubuntu@nikola-devbox:~$ cd sites
> ubuntu@nikola-devbox:~/sites$ ls
> README.md
> ubuntu@nikola-devbox:~/sites$ 

At this point add content by following the instructions in the
sites/README.md file in the *nikola-devbox* vm.
