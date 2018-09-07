Gaufrette
=========

Gaufrette provides a filesystem abstraction layer.

[![Build Status](https://img.shields.io/travis/KnpLabs/Gaufrette/master.svg?style=flat-square)](http://travis-ci.org/KnpLabs/Gaufrette)
[![AppVeyor Status](https://img.shields.io/appveyor/ci/NiR-/Gaufrette/master.svg?style=flat-square)](https://ci.appveyor.com/project/NiR-/gaufrette)
[![Quality Score](https://img.shields.io/scrutinizer/g/KnpLabs/Gaufrette.svg?style=flat-square)](https://scrutinizer-ci.com/g/KnpLabs/Gaufrette)
[![Packagist Version](https://img.shields.io/packagist/v/KnpLabs/Gaufrette.svg?style=flat-square)](https://packagist.org/packages/KnpLabs/Gaufrette)
[![Total Downloads](https://img.shields.io/packagist/dt/KnpLabs/Gaufrette.svg?style=flat-square)](https://packagist.org/packages/KnpLabs/Gaufrette)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)
[![Join the chat at Gitter](https://img.shields.io/gitter/room/nwjs/nw.js.svg?style=flat-square)](https://gitter.im/KnpLabs/Gaufrette)

Why use Gaufrette?
------------------

Imagine you have to manage a lot of medias in a PHP project. Lets see how to
take this situation in your advantage using Gaufrette.

The filesystem abstraction layer permits you to develop your application without
the need to know where all those medias will be stored and how.

Another advantage of this is the possibility to update the files location
without any impact on the code apart from the definition of your filesystem.
In example, if your project grows up very fast and if your server reaches its
limits, you can easily move your medias in an Amazon S3 server or any other
solution.

### Documentation

Read the official [Gaufrette documentation](http://knplabs.github.io/Gaufrette/).

### Metapackages for adapters

Every maintained adapter now have a dedicated metapackage. You can [find the list on packagist](https://packagist.org/packages/gaufrette/).
**We highly recommend you to use them as they contain their own requirements**: you don't need to worry about third-party dependencies
to install before using Gaufrette anymore.

### Symfony integration

Symfony integration is available through [KnpLabs/KnpGaufretteBundle](https://github.com/KnpLabs/KnpGaufretteBundle).

### Maintainers

Here is the list of dedicated maintainer(s) for every adapter not deprecated. If you don't receive any response to
your issue or pull request in a timely manner, ping us:

| Adapter            | Referent                    |
|--------------------|-----------------------------|
| AwsS3              | @NiR-                       |
| AzureBlobStorage   | @NiR-                       |
| DoctrineDbal       | @pedrotroller, @NicolasNSSM |
| Flysystem          | @nicolasmure                |
| Ftp                | @fabschurt                  |
| GoogleCloudStorage | @AntoineLelaisant           |
| GridFS             | @NiR-                       |
| InMemory           |                             |
| Local              |                             |
| OpenCloud          | @NiR-                       |
| PhpseclibSftp      | @fabschurt                  |
| Zip                |                             |

For `InMemory`, `Local` and `Zip` adapters everyone in this list is considered as a maintainer.

### Development

Requires the latest versions of :
  * docker-ce
  * docker-compose

1) Create `.env` file :
```bash
$ make dev
```
and configure it as you want.

2) Install dependencies :
```bash
$ make install-deps
```

3) Run tests :
```bash
$ make tests
```

You can also use a different php version, simply set the `PHP_VERSION` env var
to any of these values when calling a make target :
- `5.6`
- `7.0`
- `7.1` (default)
See the [`docker-compose.yml`](/docker-compose.yml) file for more details.

You'll need to clear the previously installed dependencies when switching from
a version to an other, to do so, run :
```bash
$ make clear-deps
$ PHP_VERSION=<the_version_you_want_to_use> make install-deps
```

### Note

This project does not have any stable release yet but we do not want to break BC now.
