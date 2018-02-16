klems.packages-installer
=========
[![Build Status](https://travis-ci.org/klems/ansible-role-packages-installer.svg?branch=master)](https://travis-ci.org/klems/ansible-role-packages-installer)

Requirements
------------
Ansible == `2.4`

Role Variables
--------------
### {{ sys_packages }}
A list that contains all the packages you want to install through your system packages manager

```
sys_packages:
  - fail2ban
  - htop
  - nginx
```

### {{ pip_packages }}
A list that contains all the packages you want to install through python-pip

```
pip_packages:
  - anguis
  - riotgen
  - bluew
```

Dependencies
------------
N/A

Example Playbook
----------------
```
- hosts: servers
  roles:
     - { role: klems.packages-installer, sys_packages: ['fail2ban', 'htop', 'nginx'] }
     - { role: klems.packages-installer, pip_packages: ['anguis', 'riotgen', 'bluew'] }
```

License
-------
BSD

Author Information
------------------
mail: klems@klems.net

