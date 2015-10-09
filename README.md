nginx
=========

This role is installing and managing Nginx.

The installation by default is done using the package. The configuration files
copied to remote based on nginx_cfg_dir variable see example below.


Role Variables
--------------

`nginx_install.package` (OPTIONAL)

This variable defines the package to install

```
defaults/main.yml

---
nginx_install:
 package: nginx
```

`nginx_cfg_dir` (REQUIRED)

This variable defines the full path to the configuration files to be copied.

Example:

```
group_vars/us-east-1a-prod-web.yml

---
nginx_cfg_dir: /etc/ansible/group_files/us-east-1a-prod-web/nginx
```

The actual directory.
```
/etc/ansible/group_files/us-east-1a-prod-web/nginx
.
├── conf.d
│   └── additional_config.conf
├── nginx.conf
├── sites-enabled
│   └── example.org
└── ssl
    ├── crt
    │   └── file1.crt
    └── key
        └── file1.key
```


License
-------

MIT


Author Information
------------------

Tal Lannder

tallannder@gmail.com
