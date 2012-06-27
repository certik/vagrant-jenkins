How to install Jenkins
======================

First create the Vagrant box::

    vagrant box add lucid32 http://files.vagrantup.com/lucid32.box
    vagrant init lucid32

Then bring it up and install Jenkins::

    vagrant up
    fab vagrant jenkins
