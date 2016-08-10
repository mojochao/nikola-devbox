# nikola-devbox

## Overview

This project provides a vagrant linux vm (ubuntu 16.04 LTS) provisioned
for use with [Nikola](https://getnikola.com/) called *nikola-devbox*.

## Installation

Clone the project somewhere and change to the project directory.

> $ git clone https://github.com/mojochao/nikola-devbox.git
> $ cd nikola-devbox

Next, setup the vagrant box.

> $ vagrant plugin install vagrant-scp
> $ vagrant plugin install vagrant-vbguest
> $ vagrant up

The *vagrant up* command will take a while, and will spew out tons of
output.  Once it finishes, copy your git configuration to the vm.

> $ vagrant scp ~/.gitconfig /home/ubuntu

At this point you have a running vm.  You can check its status.

> $ vagrant status
> Current machine states:
> 
> default                   running (virtualbox)
> 
> The VM is running. To stop this VM, you can run `vagrant halt` to
> shut it down forcefully, or you can run `vagrant suspend` to simply
> suspend the virtual machine. In either case, to restart it again,
> simply run `vagrant up`.
> $

At this point, if the vm is running, you can connect to it.

> $ vagrant ssh
> Welcome to Ubuntu 16.04.1 LTS (GNU/Linux 4.4.0-31-generic x86_64)
> 
>  * Documentation:  https://help.ubuntu.com
>  * Management:     https://landscape.canonical.com
>  * Support:        https://ubuntu.com/advantage
> 
>   Get cloud support with Ubuntu Advantage Cloud Guest:
>     http://www.ubuntu.com/business/services/cloud
> 
> 11 packages can be updated.
> 9 updates are security updates.
> 
> 
> Last login: Wed Aug 10 02:22:20 2016 from 10.0.2.2
> $ 

Now you can add content by following the instructions in the
sites/README.md file.

When you are done with the vm, shut it down.

> $ vagrant halt
> ==> default: Attempting graceful shutdown of VM...
> $

Remember to start it with the *vagrant up* in the future before use.
