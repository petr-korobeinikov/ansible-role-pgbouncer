[![Build Status](https://travis-ci.org/pkorobeinikov/ansible-role-pgbouncer.svg?branch=master)](https://travis-ci.org/pkorobeinikov/ansible-role-pgbouncer)

ansible-role-pgbouncer
======================

Pgbouncer installation.

Requirements
------------

You must provide your own `pgbouncer.ini.j2` and `userlist.txt.j2` templates.

Role Variables
--------------

* `pgbouncer_package_version` is an exact package version, e.g. `1.7.2-1.pgdg14.04+1`
* `pgbouncer_pgbouncer_ini_template` is a path to `pgbouncer.ini.j2` template within current playbook.
* `pgbouncer_userlist_txt_template` is a path to `userlist.txt.j2` template within current playbook.

Dependencies
------------

None.

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: pkorobeinikov.pgbouncer
          pgbouncer_package_version: 1.7.2-1.pgdg14.04+1
          pgbouncer_pgbouncer_ini_template: pgbouncer/pgbouncer.ini.j2
          pgbouncer_userlist_txt_template: pgbouncer/userlist.txt.j2


License
-------

BSD, MIT
