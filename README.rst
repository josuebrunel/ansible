My Ansible
==========

A repository containing a couple roles to help me setup my working directory
and handle some services on my servers


The *home* playbook
-------------------

This playbook is used to set up my home directory on a remote host

.. code:: shell

    $ ansible-playbook --ask-vault -i inventory/<target>.yml home.yml --extra-vars "xhosts=<remote_host> xuservars=<remote_user>" --user root


Variables used for *home* playbook can bed defined in *vars/home/<user>.yml* as follow:

.. code:: yaml

    target_username: 'foo'
    pypirc_username: 'foo'
    pypirc_password: 'bar'
    gitconfig_name: 'foo'
    gitconfig_email: 'foo@foo.org'
    ssh_keys:
        - MY AWESOME RSA ID PUB
