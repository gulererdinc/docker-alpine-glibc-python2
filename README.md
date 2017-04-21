Alpine GNU C library (glibc) + Python 2.7 Docker image
======================================================

This image is based on Alpine Linux image, which is only a 5MB image, and contains [Python 2.7](https://www.python.org/) and glibc to enable proprietary projects compiled against glibc (e.g. OracleJDK, Anaconda) work on Alpine.

This image includes some quirks to make [glibc](https://www.gnu.org/software/libc/) work side by
side with musl libc (default in Apline Linux). glibc packages for Alpine Linux are prepared by
[Andy Shinn](https://github.com/andyshinn) and the releases are published in
[andyshinn/alpine-pkg-glibc](https://github.com/andyshinn/alpine-pkg-glibc) github repo.


Usage Example
-------------

```bash
$ docker run --rm banzzaj/alpine-glibc-python2 python -c 'print u"Hello World"'
```

Once you have run this command you will get printed 'Hello World' from Python!

NOTE: `pip` is also available in this image.
