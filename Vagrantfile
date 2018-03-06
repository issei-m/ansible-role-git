# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "el" do |el|
    el.vm.box = "centos/7"
    el.vm.network :private_network, ip: "192.168.33.200"
    el.vm.network :forwarded_port, guest: 22, host: 2022, id: "ssh"
    el.ssh.insert_key = false
  end

  config.vm.define "ubuntu" do |ubuntu|
    ubuntu.vm.box = "ubuntu/trusty64"
    ubuntu.vm.network :private_network, ip: "192.168.33.201"
    ubuntu.vm.network :forwarded_port, guest: 22, host: 2122, id: "ssh"
    ubuntu.ssh.insert_key = false
  end
end
