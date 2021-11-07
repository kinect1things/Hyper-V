Role Name
=========

hyperv

This role is used to create, destroy, stop, and start a Hyper-V virtual machines. It was created following glenndehaan's source.

  ![glenndehaan](https://github.com/glenndehaan/ansible-win_hyperv_guest)

Requirements
------------

- administrative rights
- hyper-v pre-installed
- vswitch setup

Role Variables
--------------

Defaults
Generation: 2
Path: V:\ROOT\HyperV\
Memory: 1024MB

Dependencies
------------

- pywinrm

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

- hosts: hyperv
  tasks:
    - name: Create a VM
      import_role:
        name: hyperv
      vars:
        vmname: test
        vmstate: present
        vmgeneration: 2
        vmmemory: 1024MB

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
