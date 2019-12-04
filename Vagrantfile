# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # parent box
  config.vm.box = "ubuntu/bionic64"
  # network config
  config.vm.network "public_network",
    :bridge => 'enp0s31f6'
end
