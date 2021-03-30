# ANSIBLE ROLE MONCHI

## Description
Ansible role for the Monchi deployment.

(See Monchi repository: https://github.com/Guilleloper/monchi)
<br/><br/>

## Prepare an Ansible environment for deploying the role
Steps to prepare an Ansible environment for deploying the role:
```
$ cd <deployment location>
$ view monchi.yml
~
---
- hosts: monchi
  become: True
  gather_facts: False
  roles:
    - monchi
...
~
$ mkdir roles
$ cd roles/
$ git clone https://github.com/Guilleloper/ansible-role-monchi
$ mv ansible-role-monchi/ monchi/
$ cd ..
```
<br/><br/>
## Deploy Monchi:
```
$ ansible-playbook monchi.yml --diff --check
$ ansible-playbook monchi.yml --diff
```
