Ansible Role: Init Host
=========

Initial remote hosts

- authorize ssh keys
- set the ansible_user passwordless sudo
- install some packages for ansible

Requirements
------------

None.

Role Variables
--------------

`ssh_pub_key_files`: A list of ssh public key file path for ssh authorization

`ssh_pub_key_contents`: A list of ssh public key content for ssh authorization


Dependencies
------------

None.

Example Playbook
----------------

```yml
- hosts: servers
  vars:
    ssh_pub_key_files:
      - ~/.ssh/id_rsa.pub
    ssh_pub_key_contents:
      - ssh-rsa AEFASFASFsalfj xxxxxxxxxxxxxxxxxxx
  roles:
    - { role: djx339.init-host }
```

License
-------

BSD

Author Information
------------------

This role was created by [Daniel D](https://github.com/djx339).
