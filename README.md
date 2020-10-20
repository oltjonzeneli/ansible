Create User
=========

Create a user and upload an ssh public key for remote authentication

Requirements
------------
 
No specific required Ansible
Need a default ssh public key or a specific key need to be called out in a variable

Role Variables
--------------
#Define the user you would like to create
user_name: default

#Define the user state present or absent
user_state: present

#Define the path to the path to ssh public key
ssh_key: ~/.ssh/id_rsa.pub

Dependencies
------------

None

Example Playbook
----------------

---
- hosts: all
  tasks:
     - include_role:
         name: create_user
       vars:
         user_name: robert
         ssh_key: ~/.ssh/id_rsa.pub



License
-------

Author Information
------------------

