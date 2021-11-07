Role Name
=========

hyperv

This role is used to create, destroy, stop, and start a Hyper-V virtual machines. It was created following glenndehaan's source.

  ![glenndehaan's github](https://github.com/glenndehaan/ansible-win_hyperv_guest)

Requirements
------------

- administrative rights
- hyper-v pre-installed
- vswitch setup

Role Variables
--------------

Defaults
- State: Started
- Generation: 2
- Path: V:\ROOT\HyperV\
- Memory: 1024MB

Power Options
- present
- absent
- started
- stopped

Dependencies
------------

- pywinrm

Example Playbook
----------------

```yaml
- hosts: hyperv
  tasks:
    - name: Create a VM
      import_role:
        name: hyperv
      vars:
        vmname: test
        vmstate: present
        vmgeneration: 2
        vmcpu: 2
        vmmemory: 1024MB
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
