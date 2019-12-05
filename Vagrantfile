# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # parent box
  config.vm.box = "ubuntu/bionic64"
  #-------------------------------------
  # VM config
  config.vm.provider "virtualbox" do |vb|
    # run VM with a GUI
    vb.gui = true
    #------------------------
    # setting VM name
    vb.name = "epps-vagrant-vm"
    #------------------------
    # limiting VM memory and CPU usage
    vb.customize ["modifyvm", :id, "--cpuexecutioncap", "50"]
    vb.memory = 8096
    vb.cpus = 2
  end
  #-------------------------------------
  # network config
  config.vm.network "public_network",
    :bridge => 'enp0s31f6'
  #-------------------------------------
  # ansible
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/playbook.yml"
    #ansible.ask_become_pass = true
    ansible.become = true
    ansible.verbose = true
  end
  #-------------------------------------
end
