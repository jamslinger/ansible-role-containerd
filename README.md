Ansible Role: Containerd
=========
This ansible role installs the containerd runtime.

Requirements
------------
None

Variables
------------
None

Example Playbook
------------
```
- hosts: all
  vars_files:
    - vars/main.yml
  roles:
    - probosmo.containerd
```

License
------------
MIT
