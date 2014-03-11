dokku-name
=========
Custom Docker container name setup for dokku (https://github.com/progrium/dokku).

Requirements
------------

Development version of dokku at or after https://github.com/progrium/dokku/commit/c77cbf1d3ae07f0eafb85082ed7edcae9e836147.

Tested on Docker 0.9

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

Inside this file list exactly one name

```bash
myname
```

The above example will result in the following arguments being passed to docker during deploy and docker run:

```bash
-name myname
```

Thanks
------

Originally based on https://github.com/Frusty/dokku-name.git (no longer available at the time of this writing)

MIT License
-------

Copyright (C) 2014 Alex Sherwin


Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
