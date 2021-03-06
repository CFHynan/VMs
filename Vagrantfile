# -*- mode: ruby -*-
# vi: set ft=ruby :

#
# Comment out/in/use as desired.
#

Vagrant.configure("2") do |config|

  # Config for the cachier: cache scope per VM and switch off auto-detection.

  config.cache.scope = :machine
  config.cache.auto_detect = false

  #
  # Linux flavours.
  #

  config.vm.define :Fedora26 do |fedora64|
    fedora64.vm.box = "bento/fedora-26"
    # Package manager 'dnf' now in use, apply: https://github.com/fgrehm/vagrant-cachier/pull/180/commits/5141e1305a91eb553fc09fdf27161390e5efab5a
    fedora64.cache.enable :dnf
  end

  config.vm.define :CentOS7 do |centos64|
    centos64.vm.box = "bento/centos-7.4"
    centos64.cache.enable :yum
  end

  config.vm.define :Oracle7 do |oracle64|
    oracle64.vm.box = "bento/oracle-7"
    oracle64.cache.enable :yum
  end

  config.vm.define :Ubuntu17 do |ubuntu64|
    ubuntu64.vm.box = "bento/ubuntu-17.04"
    ubuntu64.cache.enable :apt
  end

  config.vm.define :Debian9 do |debian64|
    debian64.vm.box = "bento/debian-9"
    debian64.cache.enable :apt
  end

  config.vm.define :openSUSE422 do |opensuse64|
    opensuse64.vm.box = "bento/opensuse-leap-42.2"
    opensuse64.cache.enable :zypper
  end

  config.vm.define :Archlinux do |archlinux64|
    archlinux64.vm.box = "archlinux/archlinux"
    archlinux64.cache.enable :pacman
  end

  #
  # BSD flavours.
  #

  config.vm.define :FreeBSD11 do |freebsd64|
    freebsd64.vm.box = "bento/freebsd-11"
  end

  # Dragonfly, OpenBSD and NetBSD - as no VB Guest Additions are present the errors shown following the check can be ignored.
  
  config.vm.define :Dragonfly46 do |dragonfly64|
    dragonfly64.vm.box = "b00ga/dragonfly46-ufs"
  end

  config.vm.define :OpenBSD56 do |openbsd64|
    openbsd64.vm.box = "tmatilai/openbsd-5.6"
  end

  config.vm.define :NetBSD7 do |netbsd64|
    netbsd64.vm.box = "kja/netbsd-7-amd64"
  end

  #
  # Ad hoc - possibly useful.
  #

  # Solaris 11

  config.vm.define :Solaris11 do |solaris64|
    solaris64.vm.box = "jonatasbaldin/solaris11"
  end

  # Container optimized distro.
  # As no VB Guest Additions are present the errors shown following the check can be ignored.

  config.vm.define :CentOSAtomic do |centosatomic64|
    centosatomic64.vm.box = "centos/atomic-host"
  end

  # CentOS with Ansible and Git.

  config.vm.define :CentOS7_AG do |centosag64|
    centosag64.vm.box = "hisa_x/centos7-ansible"
    centosag64.cache.enable :yum
  end

  # Ubuntu with Puppet.

  config.vm.define :Ubuntu14_Pup do |ubuntupup64|
    ubuntupup64.vm.box = "puppetlabs/ubuntu-14.04-64-puppet"
    ubuntupup64.cache.enable :apt
  end

end

####################

# Usage.

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

# The most common configuration options are documented and commented below.
# For a complete reference, please see the online documentation at
# https://docs.vagrantup.com.

# Every Vagrant development environment requires a box. You can search for
# boxes at https://vagrantcloud.com/search.
  
# Disable automatic box update checking. If you disable this, then
# boxes will only be checked for updates when the user runs
# `vagrant box outdated`. This is not recommended.
# config.vm.box_check_update = false

# Create a forwarded port mapping which allows access to a specific port
# within the machine from a port on the host machine. In the example below,
# accessing "localhost:8080" will access port 80 on the guest machine.
# NOTE: This will enable public access to the opened port
# config.vm.network "forwarded_port", guest: 80, host: 8080

# Create a forwarded port mapping which allows access to a specific port
# within the machine from a port on the host machine and only allow access
# via 127.0.0.1 to disable public access
# config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

# Create a private network, which allows host-only access to the machine
# using a specific IP.
# config.vm.network "private_network", ip: "192.168.33.10"

# Create a public network, which generally matched to bridged network.
# Bridged networks make the machine appear as another physical device on
# your network.
# config.vm.network "public_network"

# Share an additional folder to the guest VM. The first argument is
# the path on the host to the actual folder. The second argument is
# the path on the guest to mount the folder. And the optional third
# argument is a set of non-required options.
# config.vm.synced_folder "../data", "/vagrant_data"

# Provider-specific configuration so you can fine-tune various
# backing providers for Vagrant. These expose provider-specific options.
# Example for VirtualBox:
#
# config.vm.provider "virtualbox" do |vb|
#   # Display the VirtualBox GUI when booting the machine
#   vb.gui = true
#
#   # Customize the amount of memory on the VM:
#   vb.memory = "1024"
# end
#
# View the documentation for the provider you are using for more
# information on available options.

# Enable provisioning with a shell script. Additional provisioners such as
# Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
# documentation for more information about their specific syntax and use.
# config.vm.provision "shell", inline: <<-SHELL
#   apt-get update
#   apt-get install -y apache2
# SHELL

####################
