# HHVM-LIVE
Config Files for creating or remastering Live-build Debian(stretch) bootable ISO for [HHVM](https://hhvm.com)

### What is HHVM

HipHop Virtual Machine (HHVM) is an open-source virtual machine based on just-in-time (JIT) compilation that serves as an execution engine for the Hack programming language.

### Bootable ISO image Embedded features

1. Debian(stretch) base
2. Nginx web server
3. PHP-FPM daemon
4. HHVM daemon
5. OpenSSH daemon
6. Some Console utilities(git, nano, composer.phar)
7. [DEB.SURY.ORG](https://deb.sury.org) Repository for PHP-DEV

### Requirement
* git
* live-build

While it's probably possible to build on other configuration, HHVM is not yet supported on Debian(buster) so this live-build configuration is designed for building HHVM-LIVE on a Debian(stretch) base.

``` sudo apt-get update;```

``` sudo apt-get install git live-build;```

### Installation

``` git clone https://github.com/yanicky/HHVM-LIVE;```

### Building the bootable ISO image
use the following commands in the base directory to build the iso

``` cd HHVM-LIVE;```

```sh auto/config; sudo lb clean; sudo lb build;```

Creating a iso file named live-image-amd64.hybrid.iso of about 420MB.

### Troubleshooting
* Secure Boot(UEFI) need to be disabled since it's not configured in the live-build config yet and will require user bios configuration to work.
