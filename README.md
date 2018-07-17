A tiny web server in C
======================

Forked from [shenfeng/tiny-web-server](https://github.com/shenfeng/tiny-web-server)

Made significantly dumber, by removing directory listing, and defaulting to hosting `index.html`.

Other relative URLs will still work, and be hosted as expected.

Features
--------

1. Basic MIME mapping
2. ~~Very basic directory listing~~
3. Low resource usage
4. [sendfile(2)](http://kernel.org/doc/man-pages/online/pages/man2/sendfile.2.html)
5. Support Accept-Ranges: bytes (for in browser MP4 playing)
6. Concurrency by pre-fork

Non-features
------------

1. No security check

Usage
-----

`tiny [port]`, opens a server in the current directory attempting to host `index.html`

`tiny <path> [port]` opens a server in relative `<path>` directory, attempting to host `index.html`

License
-------

The code is free to use under the terms of the MIT license.
