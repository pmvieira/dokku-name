dokku-dns
=========

Custom DNS setup for dokku (https://github.com/progrium/dokku).

Requirements
------------

Development version of dokku at or after https://github.com/progrium/dokku/commit/c77cbf1d3ae07f0eafb85082ed7edcae9e836147.

Installation
------------

```bash
$ cd /var/lib/dokku/plugins
$ sudo git clone https://github.com/Frusty/dokku-dns.git dns
````

Usage
-----

In your applications folder (/home/dokku/app_name) create a file called DNS.

Inside this file list one DNS IP*. For example:

```bash
8.8.8.8
8.8.4.4
```

The above example will result in the following arguments being passed to docker during deploy and docker run:

```bash
-dns 8.8.8.8 -dns 8.8.4.4
```

Thanks
------

This plugin is heavily based on the persistent-storage-plugin.
https://github.com/dyson/dokku-persistent-storage

License
-------

MIT.