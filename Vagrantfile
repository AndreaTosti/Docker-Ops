# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.box_check_update = false
  config.vm.box_version = "2004.01"

  config.vm.provider :libvirt do |libvirt|
    libvirt.memory = 2048
    libvirt.cpus = 1
    libvirt.driver = "kvm"
    libvirt.connect_via_ssh = false
    libvirt.uri = "qemu:///system"
    libvirt.storage_pool_name = "default"
    libvirt.qemu_use_session = false
    libvirt.machine_virtual_size = 42
  end

  # VM CentOS 1
  config.vm.define "docker1" do |docker|
    docker.vm.hostname = "docker1.local"
    docker.vm.network :private_network, ip: "192.168.60.4"
  end

  # VM CentOS 2
  config.vm.define "docker2" do |docker|
    docker.vm.hostname = "docker2.local"
    docker.vm.network :private_network, ip: "192.168.60.5"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
    ansible.verbose = "vvv"
  end

end
