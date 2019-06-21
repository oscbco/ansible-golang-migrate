Role Name
=========

Execute migrations with golang-migrate

Requirements
------------

Role Variables
--------------

userdba: OS User responsible for executing the migrations, must have the proper permissions in the target database
appdir: the parent dir of the migrations directory
db: Name of the database

Extra Variables
---------------
force: The version of migrations to be "forced"
down: Execute down migrations
up: Execute up migrations

Dependencies
------------

Example Playbook
----------------

    - hosts: servers
      roles:
        - {
            role: oscbco.sequelize_migrate,
            userdba: "{{ global_userdba }}",
            appdir: "{{ global_appdir }}"
          }

License
-------

MIT

Author Information
------------------

oscbco.me
