# -*- mode: ruby -*-
# vi: set ft=ruby :

imagen = "geerlingguy/ubuntu2004"

Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", disabled: true

  config.vm.define "ftp" do |f|
    f.vm.box = imagen
    f.vm.network "public_network"
    f.vm.hostname = "ftp"
  end

  config.vm.provider :virtualbox do |vbox|
    vbox.name = "ftp"
    vbox.memory = 4096
    vbox.cpus = 2
  end
end



