# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
      config.vm.define "web" do |web|	  
      web.vm.box = "generic/ubuntu2004"
      web.vm.network "private_network", ip: "192.168.56.30"
      web.vm.synced_folder "./backup", "/vagrant_data"
      web.vm.provider "virtualbox" do |vb|
        vb.memory = "1024"
        vb.cpus = 2
        end
  
      web.vm.provision "shell", path: "install_package"
  
      end

      config.vm.define "sql" do |sql|
      sql.vm.box = "ubuntu/focal64"
      sql.vm.network "private_network", ip:"192.168.56.35"
      sql.vm.provider "virtualbox" do |vb|
         vb.memory = "2048"
         vb.cpus = 2
         end

     sql.vm.provision "shell", inline: <<-SHELL
     SHELL
    end
end
