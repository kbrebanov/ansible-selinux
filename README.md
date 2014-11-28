selinux
=======

Configures SELinux.

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

Dependencies
------------

Example Playbook
----------------

Configures SELinux in permissive mode.

    - hosts: all
      roles:
         - { role: selinux }

License
-------

BSD

Author Information
------------------

Kevin Brebanov
