# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.55.166"
  config.vm.synced_folder "./code", "/var/www"

  config.vm.provider :virtualbox do |vb|
    vb.memory = 2048
    vb.cpus = 2
  end

  config.vm.provision "ansible" do |ansible|
    #ansible.verbose = 'v'
    ansible.playbook = "./provisioning/playbook.yml"
    ansible.inventory_path = "./provisioning/inventory"
  end
end