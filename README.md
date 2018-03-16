Ansible Role: Nextcloud
=========

Ansible role that installs [nextcloud](https://nextcloud.com), a open source self-hosted file share and communication platform, on Debian based systems.

**Currently, only the MySQL backend is supported with this role.**


Requirements
------------

None

Role Variables
--------------

A brief description of the variables that are required by this role (You can define those under `defaults/main.yml`)

```YAML
# Which nextcloud version to use (Default is 13.0.0)
nextcloud_version: "13.0.0"

# Which webroot to use for nextcloud (default is /var/www/)
nextcloud_webroot: "/var/www/"

# Wether the MySQL password for root should be changed (default is true)
mysql_change_root_password: true

# Password for the MySQL root user (Will only be set if mysql_change_root_password is set to true)
mysql_root_password: "root"

# Username for the new MySQL account that will be used by nextcloud (default is nextcloud)
mysql_nextcloud_user_name: "nextcloud"

# Password for the new MySDQL account that will be used by nextcloud (default is nextcloud)
mysql_nextcloud_user_password: "nextcloud"

# MySQL database that will be created and used by nextcloud (default is nextcloud)
mysql_nextcloud_db: "nextcloud"

# Username for the user that will be used to login to the nextcloud application (default is nextcloud)
nextcloud_user_name: "nextcloud"

# Password for the user that will be used to login to the nextcloud appliaction (default is nextcloud)
nextcloud_user_password: "nextcloud"

# Which data directory nextcloud should use (default is /var/www/nextcloud/data)
nextcloud_data_directory: "/var/www/nextcloud/data"
```

Dependencies
------------

None

License
-------

MIT

TODO
----
- Add PostgreSQL support
- Add SSL support
- Add NGINX support

Author Information
------------------

This role was created by [iTeV](https://github.com/iTeV)
