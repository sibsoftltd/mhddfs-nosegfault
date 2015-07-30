# mhddfs-nosegfault
Mhddfs without a 'Transport endpoint is not connected' bug which was introduced in 0.1.39. This repository will be discounted as soon as I'll receive a response from maintainer.

## Preamble

Here are some descriptions of that issue which I've found across the internets. If you've found this repository while searching a solution for that one then you're in a right place.

https://bugs.launchpad.net/ubuntu/+source/mhddfs/+bug/1429402

http://serverfault.com/questions/677352/mhddfs-randomly-breaks

http://stackoverflow.com/questions/24966676/transport-endpoint-is-not-connected

http://stackoverflow.com/questions/18006602/mhddfs-automount-failure-and-home-disconnection 

## Installation

CentOS
```nohighlight
yum install git fuse fuse-devel glib2-devel gcc make libattr-devel
git clone https://github.com/vdudouyt/mhddfs-nosegfault/
make && cp mhddfs /usr/bin/
```

Debian
```nohighlight
fakeroot dpkg-buildpackage
```

## FUSE version concerns

It was reported that sometimes, mhddfs exits with the following error due to an internal bug in FUSE. It's highly suggested to use at least version 2.9.4 of FUSE in order to avoid that.

```nohighlight
fuse internal error: node 2238037 not found
```
