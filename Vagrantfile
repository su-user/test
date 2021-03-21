# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "debian/stretch64"
  config.vm.disk :disk, size: "10GB", primary: true
  config.vm.network "forwarded_port", guest: 80, host: 80
  config.vm.network "forwarded_port", guest: 8888, host: 8888
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "playbook.yml"    
   end


  config.vm.provider "virtualbox" do |vb|
     vb.memory = "2048"
	 vb.cpus = 2
   end
end
