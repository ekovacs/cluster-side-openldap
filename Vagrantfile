# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "base"
  config.vm.box_check_update = false


 config.vm.define "centos_7" do |centos_7|
    centos_7.vm.box = "centos/7"
    config.vm.provider "virtualbox" do |v|
      v.memory = 1024
      v.cpus = 1
    end
  end

  config.vm.define "debian_9" do |debian_9|
    debian_9.vm.box = "generic/debian9"
    config.vm.provider "virtualbox" do |v|
      v.memory = 1024
      v.cpus = 1
    end
  end

  config.vm.define "ubuntu_16" do |ubuntu_16|
    ubuntu_16.vm.box = "ubuntu/xenial64"

    # python2 is needed for ansible
    ubuntu_16.vm.provision "shell", inline: "apt-get update && apt-get install python -y"

    config.vm.provider "virtualbox" do |v|
      v.memory = 1024
      v.cpus = 1
    end
  end

end
