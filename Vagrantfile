# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "gentoo-amd64"

    # vagrant plugin install vagrant-disksize
    config.disksize.size = "40GB"
  
  config.vm.box_check_update = false

  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.synced_folder "./work", "/work"
  #config.vm.synced_folder ".", "/vagrant", type: "nfs"
  
   config.vm.provider "virtualbox" do |vb|
     vb.name = "gentoo-amd64"
     vb.gui = false
     vb.memory = "8192"
     vb.cpus = "2"
   end
 
 config.vm.provision "shell", path: "./scripts/provision.sh"
end
