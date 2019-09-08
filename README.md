# HHVM-LIVE
Config Files for creating or remastering Live-build Debian(stretch) bootable ISO for [HHVM](https://hhvm.com)

### What is HHVM

HipHop Virtual Machine (HHVM) is an open-source virtual machine based on just-in-time (JIT) compilation that serves as an execution engine for the Hack programming language.

### Bootable ISO image Embedded features

0. Debian(stretch) base
1. Nginx web server
2. PHP-FPM daemon
3. HHVM daemon
4. OpenSSH daemon
5. Docker-ce daemon
6. Some Console utilities(git, nano, composer.phar)
7. [DEB.SURY.ORG](https://deb.sury.org) Repository for PHP-DEV
8. NodeJS 10.X
9. Special Tweak(hhvm.conf) that force NGINX to use use PHP-FPM instead of HHVM to process .PHP files.

### Requirement
* git
* live-build

While it's probably possible to build on other configuration, HHVM is not yet supported on Debian(buster) so this live-build configuration is designed for building HHVM-LIVE on a Debian(stretch) base.

``` sudo apt-get update;```

``` sudo apt-get install git live-build;```

### Installation methods

1. (recommended) ``` git clone https://github.com/yanicky/HHVM-LIVE; cd HHVM-LIVE;```
``` ```
2. (other) ``` mkdir HHVM-LIVE; cd HHVM-LIVE; lb config --config=https://github.com/yanicky/HHVM-LIVE```


### Building the bootable ISO image
use the following commands in the base directory(HHVM-LIVE) to build the iso

```sh auto/config; sudo lb clean; sudo lb build;```

Creating a iso file named live-image-amd64.hybrid.iso of about 592MB.

### Remastering
Optional configuration files are placed in opt/ just copy them in config/proper/subfolder before running the build command.

### Troubleshooting
* Secure Boot(UEFI) need to be disabled since it's not configured in the live-build config yet and will require user bios configuration to work.
