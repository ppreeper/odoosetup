# OdooSetup

This repository allows you to use ansible as a sysadmin tool to deploy common software setups.

You can manage your targets of hosts and clusters and can contribute back into the common repository with new recipes.

## Odoo General Variables

The general service assumption is that Cloudflare is being use to do a DNS TLS key with Caddy.

```
POSTGRES_VERSION: 15
user: "odoo"
gid: 1001
uid: 1001
home: "/home/odoo"
odoo_dir: "/opt/odoo"
odoo_config: "/opt/odoo/conf"
odoo_data: "/opt/odoo/data"
odoo_addons: "/opt/odoo/addons"
odoo_backups: "/opt/odoo/backups"
cluster_db: 10.0.0.1
cluster_fs: 10.0.0.2
cluster_logger: 10.0.0.3
cloudflare_key: secret_key
```

## Odoo Host Variables

```
odoo.example.com:
name: odoo.example.com
project: "odoo17"
odoo_version: 17.0
odoo_server_mode: server
odoo_enterprise: false
odoo_admin_passwd: admin
odoo_db_host: 127.0.0.1
odoo_db_port: 5432
odoo_db_name: odoo17
odoo_db_username: odoo
odoo_db_password: odoo
odoo_log_level: debug
```
