Role Name
=========

[![Build Status](https://travis-ci.org/patrick-hill/ansible-role-remmina.svg?branch=master)](https://travis-ci.org/patrick-hill/ansible-role-remmina)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-patrick--hill.remmina-blue.svg)](https://galaxy.ansible.com/patrick-hill/remmina)


Installs [Remmina](http://www.remmina.org/wp/) VNC on Debian based OS

Requirements
------------

Ansible 2.0+

Role Variables
--------------

    os_username
"os_username" is the target user name used for pathing

    remmina_use_backup
"remmina_use_backup" boolean to decide if using backup

    remmina_use_backup_symlink
"remmina_use_backup_symlink" boolean to decide if backup is a symlink

    remmina_config_dir
"remmina_config_dir" defaults to:  `"/home/{{ os_username }}/.remmina"`

    remmina_backup_dir
"remmina_backup_dir" is the backup directory

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: development-machines
      roles:
        - { role: patrick-hill.remmina}

*Inside `vars/main.yml`*:

    os_username: phill
    remmina_use_backup: true
    remmina_use_backup_symlink: true
    remmina_config_dir: "/home/{{ os_username }}/.remmina"
    remmina_backup_dir: "{{ backup_dir_root }}/configs/remmina"
    
License
-------

BSD

Author Information
------------------

Role written in 2016 by [Patrick Hill](http://www.HillsPCWorld.com) 