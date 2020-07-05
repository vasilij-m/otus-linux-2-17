# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"
  config.vbguest.auto_update = false

  config.vm.define "server" do |server|
    server.vm.network "private_network", ip: "192.168.10.10"
    server.vm.provider "virtualbox" do |v|
      v.memory = 1024
      v.cpus = 1
    end
    server.vm.hostname = "server"
  end

  config.vm.define "backup" do |backup|
    backup.vm.network "private_network", ip: "192.168.10.20"
    backup.vm.provider "virtualbox" do |v|
      v.memory = 1024
      v.cpus = 1
    end
    backup.vm.hostname = "backup"
  end

end
