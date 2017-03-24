# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "kb1" do |kb1|
    kb1.vm.box = "ubuntu/xenial64"
    kb1.vm.hostname = "kb1"
    kb1.vm.network "forwarded_port", guest: 5601, host: 5000
    kb1.vm.network "private_network", ip: "192.168.50.101"
    kb1.vm.provision :shell, inline: "apt-get -qqy install python"
    kb1.vm.provider "virtualbox" do |v|
      v.name = "kb1"
      v.memory = 4096
    end
  end

  config.vm.define "es1" do |es1|
    es1.vm.box = "ubuntu/xenial64"
    es1.vm.hostname = "es1"
    es1.vm.network "private_network", ip: "192.168.50.110"
    es1.vm.provision :shell, inline: "apt-get -qqy install python"
    es1.vm.provider "virtualbox" do |v|
      v.name = "es1"
      v.memory = 2048
    end
  end

  config.vm.define "es2" do |es2|
    es2.vm.box = "ubuntu/xenial64"
    es2.vm.hostname = "es2"
    es2.vm.network "private_network", ip: "192.168.50.111"
    es2.vm.provision :shell, inline: "apt-get -qqy install python"
    es2.vm.provider "virtualbox" do |v|
      v.name = "es2"
      v.memory = 2048
    end
  end

end
