
# Quick intro

This repo contains a few files which were originally from http://gnunet.org/knock and needed some changes for my tests.

# Kernel patch

The patch for the kernel actually works now with 3.18. The one on the project website was built against 3.18rc3.

# OpenSSH (for Linux) patch

The patch for the Linux OpenSSH got more changes. Please follow this procedure to use it.

```
$ tar xjz </path/to/openssh-6.7p1.tar.gz>
$ cd openssh-6.7p1
$ patch -p1 < </path/to/openssh-linux-knock-patch.diff>
$ export CFLAGS=" -DHAVE_TCP_STEALTH=26"
$ ./configure
$ make
$ make install 
```

