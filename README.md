SuiteCRM
======

Installs [SuiteCRM](http://suitecrm.com/) using Nginx.

Requirements
------------

This role was created on/for Ubuntu Trusty installations and was specifically tested in an OpenVZ container environment.

You must download the SuiteCRM-7.7.1.zip file from the SuiteCRM site and place it in files/ before using this role.  SuiteCRM requires registration and login to download files.

Role Variables
--------------

The role uses the following variables, set in the defaults/main.yml file:

* `suitecrm_version` - Specific version of SuiteCRM to install (defaults to 7.7.1)
* `suitecrm_install_dir` - Directory to install SuiteCRM (defaults to /var/www)
* `suitecrm_frontend_host` - Hostname of SuiteCRM install (defaults to localhost)
* `suitecrm_database_host` - Hostname of MySQL database (defaults to localhost)
* `suitecrm_database_user` - SuiteCRM database username (defaults to suitecrm_admin)
* `suitecrm_database_password` - SuiteCRM database user password (defaults to ise982nxk)
* `suitecrm_timezone` - SuiteCRM server timezone (defaults to America/Los_Angeles)

Dependencies
------------

Depends on the mysql module of Ansible, yet included

Example Playbook
-------------------------

Example playbook for installing SuiteCRM database and web servers on standalone system:

    ---
    - hosts: crm
      roles:
        - { role: ansible-suitecrm }
      vars:
        - suitecrm_database_user: admin
        - suitecrm_database_password: AdminSuiteCRM
        - suitecrm_frontend_host: localhost

License
-------

MIT

Author Information
------------------

Created by Gary Arnold

Updated by paulbsd

[GitHub project page](https://github.com/paulbsd/ansible-suitecrm)
