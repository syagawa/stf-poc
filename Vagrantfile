# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  # config.vm.network "forwarded_port", guest: 22, host: 2201, id: "ssh"
  config.vm.network "forwarded_port", guest: 80, host: 3001
  (7400..7700).each do | n |
    config.vm.network "forwarded_port", guest: n, host: n
  end

  config.vm.network "public_network", ip: "change me"

  config.vm.synced_folder ".", "/vagrant", type: "virtualbox"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "4096"
    vb.customize [
      "usbfilter",
      "add", "0",
      "--target", :id,
      "--name", "all"
    ]
  end
end
