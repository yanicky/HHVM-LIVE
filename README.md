# HHVM-LIVE
Config Files for creating Live-build Debian(stretch) bootable ISO for [HHVM](https://hhvm.com)

### Requirement

While it's probably possible to build on other configuration, HHVM is not yet supported on Debian(buster) so this live-build configuration is designed for building HHVM-LIVE on Debian(stretch) and require live-build to be installed.

### Installation

``` git clone https://github.com/yanicky/HHVM-LIVE;```


use the following commands in the base directory to build the iso

``` cd HHVM-LIVE```

```lb config; sudo lb clean; sudo lb build;```

Creating a iso file named live-image-amd64.hybrid.iso of about 420MB.
