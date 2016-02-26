nginx
=========

role to install and managing Nginx.

The installation by default is done using the package.


Role Variables
--------------

`nginx_conf` (OPTIONAL)

  The main nginx configuration file (relative or full path).


`nginx_sites_enabled` (OPTIONAL)

  Relative or full path to sites-enabled folder any files from that directory
  will be copied to remote.


`nginx_conf_d` (OPTIONAL)

  Relative or full path to additional configuration files will be copied to
  remote's conf.d directory.

`nginx_ssl_keys` and `nginx_ssl_certs` (OPTIONAL)

   Relative or full path to directories to copy the SSL keys and certs from.

```
defaults/main.yml

nginx_install:
 type: pkg # can be src or pkg
 # Following variables only for installation from source
 src_file: http://nginx.org/download/nginx-1.9.5.tar.gz
 src_file_sha256: 48e2787a6b245277e37cb7c5a31b1549a0bbacf288aa4731baacf9eaacdb481b
```

License
-------

MIT


Author Information
------------------

Tal Lannder

tal@pjili.org
