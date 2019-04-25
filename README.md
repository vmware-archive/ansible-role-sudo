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
- hosts: sudohosts
  sudo: True
  connection: local
  roles:
    - sudo
  vars_files:
    - vars/sudousers.yml
```

# License and Copyright
 
Copyright © 2015 VMware, Inc. All Rights Reserved.

SPDX-License-Identifier: Apache-2.0 OR GPL-3.0-only

This code is Dual Licensed Apache License 2.0 or GPLv3

You may obtain a copy of the License(s) at

    http://www.apache.org/licenses/LICENSE-2.0

    or

    https://www.gnu.org/licenses/gpl-3.0.en.html

## Author Information

This role was created in 2015 by [Tom Hite / VMware](http://www.vmware.com/).
