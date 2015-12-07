# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  # Set Vagrant box type
  config.vm.box = "centos/7"

  # Forward port TCP/4000 from the host to guest port TCP/4000, allowing for access to the Jekyll development server via http://localhost:4000 in your host's browser
  config.vm.network "forwarded_port", guest: 4000, host: 4000

  # Disable syncing of /vagrant folder
  config.vm.synced_folder ".", "/vagrant", disabled: true

  # Run Ansible provisioner on ./provisioning/playbook.yml
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/playbook.yml"
  end
end
