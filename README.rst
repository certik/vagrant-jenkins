About
=====

We use Fabric (http://fabfile.org/) to fully automate Jenkins
(http://jenkins-ci.org/) install. We currently install into an Ubuntu virtual
image managed by Vagrant (http://vagrantup.com/), but any Ubuntu server should
work.

How to install Jenkins
======================

Install Vagrant by installing the deb package from http://vagrantup.com/ (click
"Download Now"). Add the executable ``/opt/vagrant/bin/vagrant`` into your
PATH. Install VirtualBox by ``apt-get install virtualbox``.

First create the Vagrant box::

    vagrant box add lucid32 http://files.vagrantup.com/lucid32.box
    vagrant init lucid32

Then bring it up and install Jenkins::

    vagrant up
    fab vagrant jenkins forward_port

Access Jenkins at: http://localhost:8080/
To install NumPy and SymPy tests, do::

    fab vagrant jenkins_add_numpy jenkins_add_sympy
