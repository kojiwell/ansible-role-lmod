lmod role
=========

This is an Ansible role that installs [Lmod](https://lmod.readthedocs.io).

Requirements
------------

```
# Tested software versions
$ molecule 6.0.2 using python 3.11 
    ansible:2.15.5
    default:6.0.2 from molecule
    docker:2.1.0 from molecule_docker requiring collections: community.docker>=3.0.2 ansible.posix>=1.4.0

# Tested distro:version
$ grep " image:" molecule/default/molecule.yml 
    image: rockylinux:8.8
```

Role Variables
--------------

Here's the list of default variables.

* lmod_repo: `https://github.com/TACC/Lmod.git`
* lmod_version: `8.7.32`
* lmod_prefix: `/apps`
* lmod_configure_options: `--prefix={{ lmod_prefix }}`

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: kojiwell.lmod }

License
-------

MIT

Author Information
------------------

Created and maintained by Koji Tanaka