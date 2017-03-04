# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
    v.name = "service"
    v.memory = 1024
    v.cpus = 2
  end
  config.vm.box = "centos/7"
  config.vm.network "private_network", ip: "192.168.10.11"
  config.vm.hostname = "service.local"
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "service.yml"
    ansible.verbose = "v"
  end
end
