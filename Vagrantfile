# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/jammy64"
  config.vm.hostname = "postfix"
  config.ssh.insert_key = false
  config.vm.network "private_network", ip: "192.168.60.3"
  config.vm.synced_folder ".", "/vagrant", disabled: true

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "512"
  end
  
  # Ansible provisioner
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
