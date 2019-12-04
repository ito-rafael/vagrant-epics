# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # parent box
  config.vm.box = "ubuntu/bionic64"
  #-------------------------------------
  # network config
  config.vm.network "public_network",
    :bridge => 'enp0s31f6'
  #-------------------------------------
  # ansible
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook/install-epics.yml"
    #ansible.ask_become_pass = true
    ansible.verbose = true
  end
  #-------------------------------------
end
