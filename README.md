Role Name: sardpost.modsecurity
=========

Ansible role for installing mod_security in Apache on EL 7 platform (RHEL/Centos 7).
It checks if Epel repository is installed and installs Apache Httpd if not already present.
The role downloads and installs the latest OWASP CRS Core Rule Set.

Requirements
------------

Platform: RHEL/Centos 7


Dependencies
------------

This role needs two roles:

    - geerlingguy.apache
    - yaegashi.blockinfile (if using Ansible 2.0 not necessary as already included in core modules)

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - name: Install Modsecurity
      hosts: modsec
      remote_user: centos
      become: yes
      become_method: sudo

      roles:
        - sardpost.modsecurity
        - yaegashi.blockinfile

Version:
--------

0.1

License
-------

GPLv3

Author Information
------------------

Davide M. Puggioni
