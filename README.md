[![No Maintenance Intended](http://unmaintained.tech/badge.svg)](http://unmaintained.tech/)

selinux
=======

[![Ansible Role](https://img.shields.io/ansible/role/3289.svg)](https://galaxy.ansible.com/list#/roles/3289)

Configures SELinux.

Requirements
------------

This role requires Ansible 1.4 or higher.

Role Variables
--------------

| Name           | Default    | Description                                       |
|----------------|------------|---------------------------------------------------|
| selinux_policy | targeted   | SELinux policy type (targeted or mls)             |
| selinux_state  | permissive | SELinux state (permissive, enforcing or disabled) |

Dependencies
------------

None

Example Playbook
----------------

Configure SELinux in permissive mode.
```
- hosts: all
  roles:
    - { role: kbrebanov.selinux }
```

Disable SELinux
```
- hosts: all
  roles:
    - { role: kbrebanov.selinux, selinux_state: disabled }
```

Configure SELinux to use mls policy and enforcing mode
```
- hosts: all
  roles:
    - { role: kbrebanov.selinux, selinux_policy: mls, selinux_state: enforcing}
```

License
-------

BSD

Author Information
------------------

Kevin Brebanov
