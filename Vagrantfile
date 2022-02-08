# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  ## Escolha da Box
  config.vm.box = "generic/ubuntu2004"

  ## Configurações da VM
  config.vm.define 'server' do |server|

    server.vm.hostname = "server"
    server.vm.provider ":libvirt" do |v|
      v.name = "server"
      v.memory = 2048
      v.cpus = 8
    end

    server.vm.provision :ansible_local do |ansible|
      ansible.install  = true
      ansible.install_mode = "default"
      ansible.playbook = "ansible/playbook.yml"
      ansible.inventory_path = "ansible/inventory"
      ansible.verbose  = true
      ansible.limit    = "all"
    end
    server.vm.synced_folder "./", "/vagrant"
  end
end
