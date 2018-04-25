# Docker CE i386

This repository adds support for building Docker CE for the i386 architecture.
Currently, only the releases Debian Stretch and Ubuntu Xenial are supported.
Other Debian and Ubuntu releases should be easy to add following those blueprints.


## Building Packages

The environment variable `ARCH` is used to specify the architecture.
To build packages for all supported releases, run
```
$ ARCH=i386 make deb
```


## Selecting a Release

If you don't want to build packages for all supported releases, you can use
the environment variable `DOCKER_BUILD_PKGS`, e.g.

```
$ ARCH=i386 DOCKER_BUILD_PKGS=debian-stretch make deb
```
or

```
$ ARCH=i386 DOCKER_BUILD_PKGS="debian-stretch ubuntu-xenial" make deb
```

This will work for other architectures, too.

For a list of releases, check the definitions of `DOCKER_BUILD_PKGS`
in `components/packaging/Makefile`
