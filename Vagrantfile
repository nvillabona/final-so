# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

    # Configuración de la máquina virtual
    config.vm.box = "ubuntu/bionic64"
    config.vm.hostname = "ubuntu-bionic"
    config.vm.network "private_network", ip: "192.168.56.10"
  
    # Asignación de recursos
    config.vm.provider "virtualbox" do |vb|
      vb.memory = 2048  # 2GB de RAM
      vb.cpus = 2       # 2 núcleos de CPU
    end
  
    # Configuración SSH 
    config.ssh.username = "vagrant"

    # Provisionamiento con Ansible
    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end
  end
  