# VMs
Repo for Vagrant boxes.

Conveniently provides mostly Linux variants and other potentially useful instances.

## Prerequisites

Vagrant, Vagrant-Cachier plugin, VirtualBox, and VirtualBox Extension Pack installs.

https://www.vagrantup.com/downloads.html
https://www.virtualbox.org/wiki/Downloads

## Notes

1. Latest versions of Fedora use package manager 'dnf', apply the following to enable caching: https://github.com/fgrehm/vagrant-cachier/pull/180/commits/5141e1305a91eb553fc09fdf27161390e5efab5a
2. BSD filesystems are not supported with VirtualBox as of this writing - not a bug.
3. CentOS Atomic, OpenBSD and NetBSD - VirtualBox Guest Additions not present - errors following the check can be ignored.
