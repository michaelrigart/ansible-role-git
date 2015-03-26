Ansible Git Role
================
[![Build Status](https://travis-ci.org/michaelrigart/ansible-role-git.svg?branch=master)](https://travis-ci.org/michaelrigart/ansible-role-git)

An ansible role for installing and configuring git.

For more information on Git, [visit the Git website](http://git-scm.com/)

Role Variables
--------------

```yaml
git_pkg_state: indicates the package state; Allowed setting: installed, latest
git_pkg_version: specify the specific package version you wish to install. When specifying a version, the state will be forced to installed. When omitting the variable or leaving it empty it will install the package as specified by the state variable
git_config: customise the global gitconfig throught the git_config dict
git_users: define all git users and customise their gitconfig
```

View the default vars - defaults/main.yml - for a more detailed example.

Example Playbook
-------------------------

```yaml
- hosts: servers
  roles:
     - { role: MichaelRigart.git, sudo: Yes }
```

License
-------

GPLv3

Author Information
------------------

Michaël Rigart <michael@netronix.be>