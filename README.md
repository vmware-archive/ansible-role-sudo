# ansible-role-sudo

[Ansible](https://github.com/ansible/ansible) role for adding
passwordless sudo rights to specified users.

## Requirements

None known.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    sudo_users:
      - { userid: vmware, group: vmware, password: "hashed_password_here" }

A list of users to which to add passwordless sudo rights.

## Example playbook

```
---
- hosts: supervio
  sudo: True
  connection: local
  roles:
    - sudo
  vars_files:
    - vars/sudousers.yml
```

## License

TBD

## Author Information

This role was created in 2015 by [Tom Hite / VMware](http://www.vmware.com/).
