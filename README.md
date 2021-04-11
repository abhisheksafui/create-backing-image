Role Name
=========

Install a libvirt backing image 

Requirements
------------

NA

Role Variables
--------------
pool: Name of the libvirt pool under which image will be installed
os_name: Name of OS. One of ubuntu,debian
os_version: For ubuntu speicfy the version '18.04' or '20.04', for debian specify the version 'buster'. Other os versions will be added. 


Dependencies
------------

NA

Example Playbook
----------------
- name: "Testing role role-create-backing-vol"
  hosts: localhost
  roles:
  - role: create-backing-image
    vars: 
      pool: default
      os_name: ubuntu
      os_version: 18.04

Create ansible.cfg:
[defaults]
roles_path=PATH_TO_DOWNLOADED_ROLE
inventory=PATH_TO_INVENTORY_FILE

Execute:
ansible-playbook -c ansible test.yml

License
-------

GPL-2.0

Author Information
------------------

Contact Abhishek Safui at abhishek6590@gmail.com
