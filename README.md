dokku-name
=========

Custom Docker container name setup for dokku (https://github.com/progrium/dokku).

Requirements
------------

Development version of dokku at or after https://github.com/progrium/dokku/commit/c77cbf1d3ae07f0eafb85082ed7edcae9e836147.

Installation
------------

```bash
cd /var/lib/dokku/plugins
git clone https://github.com/alex-sherwin/dokku-name.git
dokku plugins-install
````

Usage
-----

In your applications folder (/home/dokku/app_name) create a file called NAME.

Inside this file list one name per line:

```bash
name1
name2
```

The above example will result in the following arguments being passed to docker during deploy and docker run:

```bash
-name name1 -name name2
```

Thanks
------

Originally based on https://github.com/Frusty/dokku-name.git (no longer available at the time of this writing)

License
-------

MIT
