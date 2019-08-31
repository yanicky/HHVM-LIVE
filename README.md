# HHVM-LIVE
Config Files for creating or remastering Live-build Debian(stretch) bootable ISO for [HHVM](https://hhvm.com)

### What is HHVM

HipHop Virtual Machine (HHVM) is an open-source virtual machine based on just-in-time (JIT) compilation that serves as an execution engine for the Hack programming language.

### Bootable ISO image Embedded features

1. Debian(stretch) base
2. Nginx web server
3. PHP-FPM daemon
4. HHVM deamon
5. OpenSSH daemon
6. Some Console utilities(git, nano)

### Requirement

While it's probably possible to build on other configuration, HHVM is not yet supported on Debian(buster) so this live-build configuration is designed for building HHVM-LIVE on Debian(stretch) and require live-build to be installed.

### Installation
``` sudo apt-get update;```

``` sudo apt-get install live-build;```

``` git clone https://github.com/yanicky/HHVM-LIVE;```

### Building the bootable ISO image
use the following commands in the base directory to build the iso

``` cd HHVM-LIVE```

```lb config; sudo lb clean; sudo lb build;```

Creating a iso file named live-image-amd64.hybrid.iso of about 420MB.
