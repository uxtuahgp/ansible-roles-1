CLickhouse
=========

Role installs Clickhouse.

Requirements
------------

No prerequisits

Role Variables
--------------

There are variables:
clickhouse_version
clickhouse_packages
clickhouse_tablename
clickhouse_dbname
clickhouse_user
clickhouse_password
clickhouse_config_path
clickhouse_users_path

Dependencies
------------


Example Playbook
----------------

    - hosts: clickhouse
      roles:
         - clickhouse

License
-------

MIT

Author Information
------------------

Alexander Dubrovsky