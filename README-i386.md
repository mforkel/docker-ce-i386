# Docker CE i386

This repository adds support for building Docker CE for the i386 architecture.
Currently, only Debian Stretch and Ubuntu Xenial are supported.
Other Debian and Ubuntu releases should be easy to add following those blueprints.


## Building Packages

The environment variable 'ARCH' is used to specify the architecture.
To build packages for all supported releases, run
```
$ ARCH=i386 make deb
```
