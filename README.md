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
 
Copyright 2015 VMware, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

## Author Information

This role was created in 2015 by [Tom Hite / VMware](http://www.vmware.com/).
