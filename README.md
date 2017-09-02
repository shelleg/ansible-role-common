Common Role
===========

This role (hopefully) is self-explanatory

Requirements
------------

A device you want to automate

Role Variables & Default values
--------------
Please note most of these default have overrides -> see ../../playbooks/group_vars/all/... for
* `common_rpm_repos: ''`   
* `common_dns_servers: ''`
* `common_packages:`
  - vim
  - epel-release
  - sysstat
  - net-tools
  - lsof
  - telnet
* `common_sudoer: false`
* `common_user: foo`
* `common_group: bar`
* `common_home_dir: "/home/{{ * common_user }}"`
* `common_pubkey: ''`

Dependencies
------------
None (ATM ...)

Example Playbook
----------------

    - hosts: all
      become: yes
      become_user: root
      roles:
        - role: shelleg.common

License
-------

MIT

Author Information
------------------

[ratchet](https://en.wikipedia.org/wiki/Ratchet_%28Transformers%29#Transformers:_Generation_1) - "You break it, I'll remake it."
